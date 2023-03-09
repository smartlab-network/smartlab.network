---
layout: default
title: participants
permalink: /participants
nav: true
---

{%- for page in site.participants -%}
  <div class="post">
        <header class="post-header">
          <h1 class="post-title">{{page.title}}</h1>
		  <p>{{page.subtitle}}</p>
        </header>

        <article>
          <div class="profile float-{%- if page.align == 'left' -%}left{%- else -%}right{%- endif -%}">
              {%- assign image_path = page.image | prepend: 'assets/img/' -%}

              {% include figure.html 
                path=image_path 
                class="img-fluid z-depth-1 rounded"
                alt=page.image -%}
				

            {%- if page.contact %}
            <div class="address">
              {{ page.contact }}
            </div>
            {%- endif %}
          </div>

          <div class="clearfix">
            {{ page.content }}
          </div>
		  
	</article>
</div>
{%- endfor %} 

