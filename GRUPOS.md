---
layout: default
title: "Comunidade no Brasil"
permalink: /gruposdepratica/
---

# Grupos de Práticas, atendimentos e contatos no Brasil


## Amapá
{% assign praticantes_am = site.data.praticantes | where: "state", "Amapá" %}
{% for member in praticantes_am  %}
- {{ member.taoname (member.name)}}
  - {{ member.city }}
  - {{ member.phone }} // {{ member.email }}
  - {{ member.links[0] }}
  - {{ member.services[0] }}
{% endfor %}
