---
excerpt: "Hydrodynamic stability studies the behaviour of flows when subject to
  perturbations."
header:
  overlay_image: /assets/images/lobedinstability2combined.jpg
  overlay_filter: 0.3
  caption: "Instability waves change characteristics when lobes are appended."
  actions:
    - label: "Learn more"
      url: "/research/"
layout: single
author_profile: true
toc: true
#classes: wide
---
Welcome to the **Wave Physics Group** at Peking University.
## Who we are?

We are an interdisciplinary group working at the frontier of fluid mechanics, acoustics and physics.

## What we do?
We are interested in understanding the physics of waves in various
fields, such as acoustics, hydrodynamic instabilities and electrodynamics. Our
ongoing projects range from jet aeroacoustics, jet instability, aerofoil
aeroacoustics to acoustic metamaterials. You can find more about our research
from the Research and Publications pages. 

## Come and join!
We seek highly motivated graduate students with a solid background in fluid mechanics,
physics, acoustics or applied mathematics to join us. Undergraduate students who are keen to 
embark on research are warmly welcome.

Various scholarships are available. Prospective students outside China can be
supported to apply for the China Government Scholarship, which covers both
tuition and maintenance fees. We seek postdocs with a strong expertise in
aeroacoustics and fluid mechanics to work on jet noise and aerofoil noise. If
you would like to know more, please [get in touch](mailto:b.lyu@pku.edu.cn){: .btn .btn--success}.


## Recent news
{% assign num = 0 %}
{% for post in site.news reversed %}
{% if num < 3 %}
{% include archive-single-recent-news.html %}
{% assign num = num | plus: 1 %}
{% endif %}
{% endfor %}
