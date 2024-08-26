
<style>
.speakers-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    background-color: #002F6C; /* Color azul */
    padding: 20px;
}

.speakers-container li {
    flex: 1 0 21%; /* Ocupa aproximadamente el 21% del ancho, ajusta según sea necesario */
    margin: 10px;
    list-style-type: none;
    text-align: center;
}

.keynote-img {
    display: block;
    width: 100%;
    height: 250px; /* Ajusta la altura según tus necesidades */
    background-size: cover;
    background-position: center;
}

h4 {
    color: white; /* Ajusta el color del texto */
    margin-top: 10px;
}
</style>

<h3 style="color: white;">Speakers</h3>
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
