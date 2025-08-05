---
layout: page
title: People - Meet out team!
---

<div class="team">
{% for person in site.data.people %}
  <div class="team-member" style="display: flex; align-items: center; margin-bottom: 20px;">
    <img src="{{ person.image }}" alt="{{ person.name }}" style="width: 150px; height: auto; margin-right: 20px;">
    <div>
      <h4>{{ person.name }}</h4>
      <p><strong>{{ person.role }}</strong></p>
      <p>{{ person.affiliation }}</p>
      <!-- <p>{{ person.intro }}</p> -->    
      <p>
        {% for link in person.links %}
          <a href="{{ link.url }}" target="_blank">{{ link.title }}</a>{% if forloop.last == false %} | {% endif %}
        {% endfor %}
      </p>
    </div>
  </div>
{% endfor %}
</div>
