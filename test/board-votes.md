---
title: Voting

---



<!-- List motions as paragraphs -->
<!-- {% assign thisdate = "now" | "%Y-%m-%d" %} -->
{% assign thisdate = "" %}
{% for motions in site.data.votes %}
{{ thisdate }}<br>
  {% if thisdate != motions.date }}
  date: {{ motions.date }}
  motions:
    {% assign thisdate = motions.date }}
  {% endif %}
     motion: {{ motions.motion }}
     result: {{ motions.result }}
     {% if motions.vote %} vote: {{ motions.vote }}.{% endif %}
{% endfor %}