---
layout: default
permalink: /university
title: smartlab.university
subtitle: Talks und Vorlesungen im smartlab.network.
description: Talks und Vorlesungen im smartlab.network.
years: [2024]
nav: true
---

<!-- _pages/publications.md -->

<h1>smartlab university</h1>

The smartlab university develops and provides continuous learning programs in and around smartlabs.
ranging from the online lectures in our smartlab.lecure series over Web- and Video-turorials to Hackathons.

<h1>Talks</h1>

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

            {%- if page.date %}              
                <div class="address">
                  {{ page.date | date_to_string }}
                  {%- if page.time %}
                     - {{ page.time }}
                  {%- endif %}                    
                </div>
            {%- endif %}


            {%- if page.online %}
                <a href="{{ page.online }}">Online link</a>                
            {%- endif %}

            {%- if page.registration %}
                <a href="{{ page.registration }}">Registration link</a>                                
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

          {%- if page.youtubeId %}
            {% include youtubePlayer.html id=page.youtubeId %}
          {%- endif %}

	</article>
</div>
{%- endfor %}

</div>
