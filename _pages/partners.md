---
layout: default
title: partner
permalink: /partner
nav: true
---

<h1> Our Partners: </h1>

{%- for page in site.partners -%}
  <div class="post">
      <header class="post-header">
          <h1 class="post-title">{{page.title}}</h1>
		  <p>{{page.subtitle}}</p>
      </header>

      <article style="padding-bottom: 5ex;">
        <div class="profile float-left">
           {%- assign image_path = page.image | prepend: 'assets/img/' -%}
           {% include figure.html path=image_path  class="img-fluid z-depth-1 rounded" alt=page.image -%}           
        </div>
        {%- if page.contact %} 
             <div class="address"> {{ page.contact }}  </div>
        {%- endif %}

        <div class="clearfix" style="text-align: justify;">         
            
            <p>{{ page.contact }}
            <p>{{ page.url }}
            <p>{{ page.content }}                          
        </div>
		<br/>
	  </article>
  </div>
{%- endfor %}
