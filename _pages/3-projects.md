---
layout: page
permalink: /projects
title: projects
description: Featured projects
---

**Featured projects**

  <br>
  <b>Please check GitHub if you are interested in codebase of any project. If the code is not available there, it means for legal reason, I cannot share it whatsoever. </b>
  <br>

<div>  
{% for project in site.projects %}

{% if project.redirect %}
<div class="project">
    <div class="thumbnail">
        <a href="{{ project.redirect }}" target="_blank">
        {% if project.img %}
        <img src="{{ project.img | prepend: site.baseurl | prepend: site.url }}"/>
        {% else %}
        <div class="blankbox"></div>
        {% endif %}    
        <span>
            <h1>{{ project.title }}</h1>
            <br/>
            <p>{{ project.description }}</p>
        </span>
        </a>
    </div>
</div>
{% else %}

<div class="project">
    <div class="thumbnail">
        <a href="{{ project.url | prepend: site.baseurl | prepend: site.url }}">
        {% if project.img %}
        <img src="{{ project.img | prepend: site.baseurl | prepend: site.url }}"/>
        {% else %}
        <div class="blankbox"></div>
        {% endif %}    
        <span>
            <h1>{{ project.title }}</h1>
            <br/>
            <p>{{ project.description }}</p>
        </span>
        </a>
    </div>
</div>

{% endif %}

{% endfor %}
</div>

<br>
<div class="center">Click on the images for more detail description.</div>
<br>



<br>
**Selected notable projects that I have worked on:**
- [NFC Reader Ticket Application :link:](https://erbipin.com/projects/3_project_nfcticketapp/){:target="_blank"}
- [Artano :link:](https://artano.io/){:target="_blank"}
- [Artamint :link:](https://artano.io/artamint){:target="_blank"}
- [Security Token Offering (STO) Platform :link:](#){:target="_blank"}
- [Decentralized Secure Cloud Storage Using Blockchain :link:](https://erbipin.com/projects/1_project/){:target="_blank"}
- [ID21 :link:](https://id21.io/){:target="_blank"}
- Deltalender
- UnivHub
- CNFT Registry
- TSSP
<br>
*\*Details of some projects are only available upon request.*

For more information and list of other projects, please 
<a href="{{ site.url }}/download/Khatiwada_Bipin_Resume.pdf" target="_blank">check my resume</a> 
or visit my [github profile](https://github.com/bipinkh){:target="\_blank"}.

