---
layout: article
title: ""
---

## International Conferences and Journals

{% for paper in site.data.ipapers %}
<div class="grid">
  <div class="cell cell--auto">
	  <div style="font-size: 1em; font-weight: bolder;">{{paper.title}}</div>
	  <div style="font-size: 1em;">
        {% for author in paper.authors %}
            {% if forloop.last != true %}
                {% if paper.num_authors == 2 %}
                    {{ author }} 
                {% else %}
                    {{ author }},
                {% endif %}
            {% elsif paper.num_authors > 1 %}
                and {{ author }}
            {% else %}
                {{ author }}
            {% endif %}
        {% endfor %}
	  </div>
	  <div style="font-size: 1em;">
	{{ paper.publisher.venue }}
	<img src="assets/calendar.png" height="16" width="16"> {{ paper.month }} {{ paper.year }}
	  </div>
  </div>
</div>

<div class="m-3"></div>
{% endfor %}


## Domestic Conferences and Journals

{% for paper in site.data.dpapers %}
<div class="grid">
  <div class="cell cell--auto">
	  <div style="font-size: 1em; font-weight: bolder;">{{paper.title}}</div>
	  <div style="font-size: 1em;">
        {% for author in paper.authors %}
            {% if forloop.last != true %}
                {% if paper.num_authors == 2 %}
                    {{ author }} 
                {% else %}
                    {{ author }},
                {% endif %}
            {% elsif paper.num_authors > 1 %}
                and {{ author }}
            {% else %}
                {{ author }}
            {% endif %}
        {% endfor %}
	  </div>
	  <div style="font-size: 1em;">
	  {{ paper.publisher.venue }}
        {% if paper.note != nil %}
            ({{paper.note}}) 
        {% endif %}
	  <img src="assets/calendar.png" height="16" width="16"> {{ paper.month }} {{ paper.year }}
	  </div>
  </div>
</div>

<div class="m-3"></div>
{% endfor %}
