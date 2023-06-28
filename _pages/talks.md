---
layout: page
permalink: /talks/
title: talks
description: Talks und Vorlesungen im Smartlab Network.
years: [2023]
nav: true
nav_order: 1

---
<!-- _pages/publications.md -->
<div class="talks">

{%- for page in site.talks reversed -%}
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

          </div>

          <div class="clearfix" style="text-align: justify;">
            {{ page.content }}
          </div>
		  <br/>
	</article>
</div>
{%- endfor %}

</div>
