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
  <img class="entry-imag" src="{{ site.baseurl }}/assets/images/profile.jpg"> 
  <div class="entry-text">
    <p> <a href="{{ site.baseurl }}/cv/" style="font-weight:bold;">Benshuai Lyu, PhD</a><br/>
    Assitant Professor<br/>
    College of Engineering<br/>
    Office: 3043 Xin Ao Engineering Blg<br/>
    Email: b.lyu@pku.edu.cn</p>
  </div>
</div>


<!--- Determine whether have at least one member in each position category,
if yes put a h3 title --->
{% for post in site.people %}
{% if post.status == "Current" %}
  {% if post.position == "Postdoctoral Scholar" %}
    {% assign currentPostdoc = true %}
  {% elsif post.position == "Group Administrator" %}
    {% assign currentGA = true %}
  {% elsif post.position == "PhD Student" %}
    {% assign currentPhD = true %}
  {% elsif post.position == "Master Student" %}
    {% assign currentMaster = true %}
  {% elsif post.position == "Undergraduate Student" %}
    {% assign currentUndergraduate = true %}
  {% endif %}
{% elsif post.status == "Former" %}
  {% assign formerGroupMember= true %}
{% endif %}
{% endfor %}

<!--- if any position has at least one member put a h3 title and emnurate--->
{% if currentGA == true %}
<h3 class="role-title">Group Administrator</h3>
{% endif %}
{% for post in site.people%}
{% if post.status == "Current" and post.position == "Group Administrator" %}
{% include archive-single-people.html %}
{% endif %}
{% endfor %}


{% if currentPostdoc== true %}
<h3 class="role-title">Postdoctoral Scholars</h3>
{% endif %}
{% for post in site.people%}
{% if post.status == "Current" and post.position == "Postdoctoral Scholar" %}
{% include archive-single-people.html %}
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

<!--- put a Category Past first only if has past members then enumerate --->
{% if formerGroupMember == true %}
## Former
{% endif %}

{% for post in site.people%}
{% if post.status=="Former" %}
  <div>
  <span style="font-weight:bold;">{{ post.name }}</span>:  {{ post.position }} between {{ post.duration}}, now work as {{ post.jobnext | default: "TBD" }}. 
  </div>
{% endif %}
{% endfor %}
