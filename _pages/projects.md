---
layout: default
title: projects
subtitle: Our ongoing and passed projects
permalink: /projects
nav: true
---

<h1>Ongoing Projects</h1>

Der einfache Wunsch (s)ein Labor zu automatisieren f&uuml;hrt Wissenschaftler:innen 
schnell zu Herausforderungen. 
Nach dem Divide-and-Conquer Ansatz brechen wir die Problemstellung auf SMARTe-Projekte
herunter, das heisst die Einzelprojekte sind *s*pezifisch, *m*essbar, *a*usf&uuml;hrbar,
*r*ealistisch, und *t*erminiert und können von Netzwerkmitgliedern und Partnern im
Rahmen von Forschungsprojekten, Abschlussarbeiten oder im Auftrag abgearbeitet werden.
Die folgende Liste gibt einen &Uuml;berblick &uuml;ber existierende und geplante Projekte
und soll einen Anreiz geben im Netzwerk eigene Projekte vorzuschlagen.

{%- for page in site.projects -%}
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

            {%- if page.start %}
                <div>

                  {{ page.start | date_to_string }}
                  {%- if page.end %}
                      -{{ page.start | date_to_string }}
                  {%- endif %}

                  {%- if page.duration %}
                       ({ page.duration })
                  {%- endif %}


                </div>
            {%- endif %}





            {%- endif %}
          </div>

          <div class="clearfix" style="text-align: justify;">
            {{ page.content }}
          </div>
		  <br/>
	</article>
</div>
{%- endfor %}
