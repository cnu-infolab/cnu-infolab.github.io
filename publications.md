---
layout: article
title: ""
---

## International Conferences and Journals


{% for paper in site.data.papers %}
    {% if paper.international == true %}
<div class="grid">
  <div class="cell cell--auto">
	  <div style="font-size: 1.1em; font-weight: bolder;">{{paper.title}}</div>
	  <div style="font-size: 1em;">
        {% for author in paper.authors %}
            {% if forloop.last != true %}
                {{ author }},
            {% elsif paper.authors[0] != author %}
                and {{author}}
            {% else %}
                {{author}}
            {% endif %}
        {% endfor %}
	  </div>
	  <div style="color: #606060; font-size: 1em;">
        {% if paper.publisher.link != nil %}
        <a href="{{ paper.publisher.link }}" style="color: #606060;" target="_blank">
            {{ paper.publisher.venue }}
        </a>
        {% else %}
            {% if paper.type == "conference" %}
                <a class="button button--info button--rounded button--sm">Conference</a>
            {% elsif paper.type == "journal" %}
                <a class="button button--primary button--rounded button--sm">Journal</a>
            {% endif %}
	    {{ paper.publisher.venue }}
        {% endif %}
	<i class="far fa-calendar-alt fa-fw"></i> {{ paper.month }} {{ paper.year }}
	  </div>
  </div>
</div>

<div class="m-3"></div>
    {% endif %}
{% endfor %}


<!--
## Domestic Publications

-->
