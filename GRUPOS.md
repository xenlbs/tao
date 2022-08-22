---
layout: default
title: "Comunidade no Brasil"
permalink: /gruposdepratica/
---

# Grupos de Práticas, atendimentos e contatos no Brasil


## Amapá
{% assign praticantes_am = site.data.praticantes | where: "state", "AM" %}
{% for member in site.data.praticantes  %}
{{ member.taoname }}
{% endfor %}
