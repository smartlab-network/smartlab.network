---
layout: default
title: partner
permalink: /partner
nav: true
---

<h1> Our Partners: </h1>

<table>

{%- for page in site.partners -%}
 <div class="post">
        <header class="post-header">
          <h2 class="post-title">{{page.title}}</h2>
		  <p>{{page.subtitle}}</p>
        </header>

        <article style="padding-bottom: 5ex;">
          <div class="profile float-{%- if page.align == 'left' -%}left{%- else -%}right{%- endif -%}">
              {%- assign image_path = page.image | prepend: 'assets/img/' -%}

              {% include figure.html
                path=image_path
                class="img-fluid z-depth-1 rounded"
                alt=page.image -%}            
          </div>
          {%- if page.contact %}
            <div class="address">
              {{ page.contact }}
            </div>
          {%- endif %}
          
          <div class="clearfix" style="text-align: justify;">
            {{ page.content }}
          </div>
		  <br/>
	</article>
</div>
{%- endfor %}