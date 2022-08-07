---
layout: article
title: ""
---

## Professor

<div class="grid">
  <div class="cell cell--auto">
	  <div style="font-size: 1em; font-weight: bolder;">
      Jongik Kim 
      <script type="text/javascript">
      var email="jongik"
      var domain="cnu.ac.kr"
      document.write("<a style=text-decoration:none href="+"mail"+"to:"+email+"@"+domain+">"+"<i class=\"fas fa-envelope fa-fw\"><\/i>"+"<\/a>")
      </script>
      <a href="https://jongikkim.github.io"><i class="fas fa-home fa-fw"></i></a>
      </div>
	  <div style="color: #606060; font-size: 1em;">
	  Department of Computer Science and Engineering
      </div>
	  <div style="color: #606060; font-size: 1em;">
	  Chungnam National University
      </div>
	  <div style="color: #606060; font-size: 1em;">
      Office: Engineering Building #5, Room #513
	  </div>
  </div>
</div>

## Student
Currently, we have no graduate student in our lab.

## Alumni
{% for member in site.data.people %}
    {% if member.alumni == true %}
<div class="grid">
  <div class="cell cell--auto">
	  <div style="font-size: 1em; font-weight: bolder;">{{member.name}}</div>
	  <div style="color: #606060; font-size: 1em;"> received {{member.degree}} in {{member.gradyear}}</div>
	  <div style="color: #606060; font-size: 1em;">
          {% if member.appointment != nil %}
              {{ member.appointment }} (the first appointment)
          {% endif %}
          </div>
  </div>
</div>

<div class="m-3"></div>
    {% endif %}
{% endfor %}
