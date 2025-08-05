---
layout: page
---
<div style="text-align: center;">
  <h2>Explore our research highlights and publications</h2>
</div>
<div class="container">
  
  <img src="{{ '/assets/img/research/highlight.png' | relative_url }}" alt="Research Highlight" class="img-fluid my-4" style="max-width: 70%; height: auto; display: block; margin: 0 auto;">

</div>

<h3>Publications:</h3>
<ol>
{% for category in site.data.publications %}
  {% for pub in category[1] %}
    <li>
      {% if pub.authors %}
        {{ pub.authors }}
      {% elsif pub.author %}
        {{ pub.author }}
      {% endif %}
      ({{ pub.year }}). {{ pub.title }}.
      {% if pub.journal %}
        <em>{{ pub.journal }}</em>, {{ pub.volume_issue }}.
      {% elsif pub.book %}
        In <em>{{ pub.book }}</em>, pp. {{ pub.pages }}.
      {% elsif pub.institution %}
        {{ pub.type }} thesis, {{ pub.institution }}.
      {% endif %}
      {% if pub.doi %}
        doi: <a href="https://doi.org/{{ pub.doi }}">{{ pub.doi }}</a>
      {% endif %}
    </li>
  {% endfor %}
{% endfor %}
</ol>
