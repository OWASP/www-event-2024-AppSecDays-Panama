<style>
.speakers-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    background-color: #f0f0f0; /* Color de fondo nuevo */
    padding: 20px;
}

.speakers-container li {
    flex: 1 0 21%; /* Ajuste de ancho */
    margin: 10px;
    list-style-type: none;
    text-align: center;
    display: flex;
    flex-direction: column;
    align-items: center;
}

.keynote-img {
    display: block;
    width: 100%;
    height: 250px; /* Ajusta la altura según sea necesario */
    background-size: cover;
    background-position: center;
    margin-bottom: 10px; /* Añadir espacio entre la imagen y el nombre */
}

h3 {
    background-color: #f0f0f0; /* Cambia el color de fondo azul a otro color */
    color: #333; /* Cambia el color del texto si es necesario */
    padding: 10px;
    text-align: center;
}

h4 {
    color: white; /* Color de texto blanco */
    background-color: rgba(0, 0, 0, 0.7); /* Fondo semitransparente para legibilidad */
    padding: 5px;
    margin: 0;
    width: 100%; /* Ajuste al ancho de la imagen */
    box-sizing: border-box;
}
</style>

<h3 style="color: white;">Ours Speakers</h3>
<ul class="speakers-container">
{% for speaker in site.data.keynotespeakers %}
    {% if speaker.name %}
        <li>
            <a href="/program/keynotes#{{ speaker.name | slugify }}" class="keynote-img"
               style="background-image: url(assets/images/speakers/{{ speaker.image | default: 'owasp_logo.png' }});">
            </a>
            <h4>{{ speaker.name }}</h4>
        </li>
    {% endif %}
{% endfor %}
</ul>
