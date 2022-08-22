---
layout: default
title: "Comunidade no Brasil"
permalink: /gruposdepratica/
---

# Grupos de Práticas, atendimentos e contatos no Brasil

{% assign praticantes_porestado = site.data.praticantes | sort: "state" %}
{% for member in praticantes_porestado %}
- {{ member.taoname (member.name)}}
  - {{ member.city }}
  - {{ member.phone }} // {{ member.email }}
{% if member.links %}
  - {{ member.links | join: ", " }}
{% endif %}
{% if member.services %}
  - {{ member.services | join: ", " }}
{% endif %}
{% endfor %}
