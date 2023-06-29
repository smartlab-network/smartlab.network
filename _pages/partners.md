---
layout: default
title: partner
permalink: /partner
nav: true
---

<h1> Our Partners: </h1>

<table>

{%- for page in site.partners -%}
 <tr> 
      <td><h2 class="post-title">{{page.title}}</h2></td>
 </tr>
 <tr> 
   <td>
         {%- assign image_path = page.image | prepend: 'assets/img/' -%}
         {% include figure.html path=image_path  class="img-fluid z-depth-1 rounded" alt=page.image -%}           
   </td>
   <td>
        {{ page.contact }}
   </td>
 </tr>
{%- endfor %}

</table>