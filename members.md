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
      document.write("<a style=text-decoration:none href="+"mail"+"to:"+email+"@"+domain+">"+"<img src=\"assets\/email.png\" height=\"18\" width=\"18\">"+"<\/a>")
      </script>
      <a href="https://jongikkim.github.io"><img src="assets/home.png" height="18" width="18"></a>
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

## Students
{% for member in site.data.people %}
    {% if member.alumni == false %}
<div class="grid">
  <div class="cell cell--auto">
	  <div style="font-size: 1em; font-weight: bolder;">{{member.name}} {{member.degree}} student</div>
  </div>
</div>

<div class="m-3"></div>
    {% endif %}
{% endfor %}
	  
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
