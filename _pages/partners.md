---
layout: default
title: partner
permalink: /partner
nav: true
---

<h1> Our Partners: </h1>

{%- assign image_path = logo-projection.jpg | prepend: 'assets/img/' -%}

{% include figure.html
    path=image_path
    class="img-fluid z-depth-1 rounded"
    alt=logo.jpg
    max-width=600 -%}            



{%- for page in site.partners -%}
 <div class="post">
        <header class="post-header">
          <h2 class="post-title">{{page.title}} - {{page.subtitle}}</h2>		  
        </header>

        <article style="padding-bottom: 5ex;">
          <div class="profile float-left">
              {%- assign image_path = page.image | prepend: 'assets/img/' -%}

              {% include figure.html
                path=image_path
                class="img-fluid z-depth-1 rounded"
                alt=page.image
                max-width=200 -%}            
          </div>
          {%- if page.contact %}
            <div class="address">
              
              Contact: {{ page.contact }}<br/>
              eMail: {{ page.email }}<br/>
              web: [{{page.title}}]({{ page.homepage }})
            </div>
          {%- endif %}          
          <div class="clearfix" style="text-align: justify;">
            {{ page.content }}
          </div>
		  <br/>
	</article>
</div>
{%- endfor %}
