---
layout: article
title: ""
---

## International Conferences and Journals


{% for paper in site.data.ipapers %}
    {% if paper.international == true %}
<div class="grid">
  <div class="cell cell--auto">
	  <div style="font-size: 1.2em; font-weight: bolder;">{{paper.title}}</div>
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
	{{ paper.publisher.venue }}
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
