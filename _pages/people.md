---
author: group
title: "People"
layout: single
permalink: /people/
author_profile: true
toc: true
#sidebar:
#  - title: "Wave Physics Group@PKU"
#    image: /assets/images/waves.jpg
#    image_alt: "iamge"
#    text: "Acoustic, electromagetic, instability waves and more"
---
## Current
<h3 class="role-title"> Principle Investigator</h3>
<div class="entry">
  <img class="entry-imag" src="/assets/images/profile.jpg"> 
  <div class="entry-text">
    <p> <a href="/cv/" style="font-weight:bold;">Benshuai Lyu, PhD</a><br/>
    Assitant Professor<br/>
    College of Engineering<br/>
    Office: 904 Kezhen Wang Blg<br/>
    Email: b.lyu@pku.edu.cn</p>
  </div>
</div>


<!--- Determine whether have at least one member in each student category,
if yes put a h3 title --->
{% for post in site.people %}
{% if post.status == "Current" %}
  {% if post.position == "PhD Student" %}
    {% assign currentPhD = true %}
  {% elsif post.position == "Master Student" %}
    {% assign currentMaster = true %}
  {% elsif post.position == "Undergraduate Student" %}
    {% assign currentUndergraduate = true %}
  {% endif %}
{% elsif post.status == "Current" %}
  {% assign previousStudent = true %}
{% endif %}
{% endfor %}

{% if currentPhD == true %}
<h3 class="role-title">PhD Students </h3>
{% endif %}
{% for post in site.people%}
{% if post.status == "Current" and post.position == "PhD Student" %}
{% include archive-single-people.html %}
{% endif %}
{% endfor %}

{% if currentMaster == true %}
<h3 class="role-title">Master Students </h3>
{% endif %}
{% for post in site.people%}
{% if post.status == "Current" and post.position == "Master Student" %}
{% include archive-single-people.html %}
{% endif %}
{% endfor %}

{% if currentUndergraduate == true %}
<h3 class="role-title">Undergraduate Students</h3>
{% endif %}

{% for post in site.people%}
{% if post.status == "Current" and post.position == "Undergraduate Student" %}
{% include archive-single-people.html %}
{% endif %}
{% endfor %}

{% if previousStudent == true %}
## Past
{% endif %}

{% for post in site.people%}
{% if post.status=="Previous" %}
  <div>
  <span style="font-weight:bold;">{{ post.name }}</span>:  {{ post.position }} between {{ post.duration}}, now at {{ post.jobnext | default: "TBD" }}. 
  </div>
{% endif %}
{% endfor %}
