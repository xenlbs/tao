---
layout: default
title: "Comunidade no Brasil"
permalink: /gruposdepratica/
---

# Comunidade no Brasil

{% assign praticantes_porestado = site.data.praticantes | sort: "state" %}
{% assign estados_ordenados = site.data.estados | sort: "name" %}
{% for estado in estados_ordenados %}
## {{ estado.name_long }}
{% for cidade in estado.cities %}
### {{ cidade.name }}
{% assign praticantesdacidade = praticantes_porestado | where: "city", {{cidade.name}} %}
{% for member in praticantesdacidade %}
- {{ member.taoname }} ({{member.name}})
{% if member.contacts %}
  - {{ member.contacts | join: " // " }}
{% endif %}
    {% if member.links %}
  - {{ member.links | join: ", " }}
    {% endif %}
    {% if member.services %}
  - {{ member.services | join: ", " }}
    {% endif %}
{% endfor %}
{% endfor %}
{% endfor %} 