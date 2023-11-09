---
layout: default
permalink: /talks
title: talks
subtitle: Talks und Vorlesungen im Smartlab Network.
description: Talks und Vorlesungen im Smartlab Network.
years: [2023]
nav: true
---

<!-- _pages/publications.md -->
<div class="talks">

{%- for page in site.talks -%}
  <div class="post">
        <header class="post-header">
          <h1 class="post-title">{{page.title}}</h1>
		  <p>{{page.subtitle}}</p>
        </header>

        <article style="padding-bottom: 5ex;">
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

            {%- if page.date %}              
                <div class="address">
                  {{ page.date | date_to_long_string }}
                  {%- if page.time %}
                     - {{ page.time }}
                  {%- endif %}                    
                </div>
            {%- endif %}

            {%- if page.location %}
              <div class="address">
                {{ page.location }}
              </div>
            {%- endif %}

          </div>

          <div class="clearfix" style="text-align: justify;">
            {{ page.content }}
          </div>
		  <br/>
	</article>
</div>
{%- endfor %}

</div>
