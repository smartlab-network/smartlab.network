---
layout: default
title: participants
permalink: /participants
nav: true
---

{% for page in site.participants %}
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
                alt=page.image
                max-width=200 -%}

            {%- if page.name -%}
                <div class="address">
                    {{ page.name }}
                </div>
            {%- endif -%}

            {%- if page.email -%}
                <div class="address">
                    <a href="mailto:{{ page.email }}">Contact</a>                    
                </div>
            {%- endif -%}

            
            {%- if page.contact -%}
                <div class="address">
                    {{ page.contact }}
                </div>
            {%- endif -%}


          </div>

          <div class="clearfix" style="text-align: justify;">
            {{ page.content }}
          </div>

          {%- if page.contact -%}
          <div class="address">
            {{ page.contact }}
          </div>
          {%- endif -%}
	</article>
</div>
{%- endfor %}
