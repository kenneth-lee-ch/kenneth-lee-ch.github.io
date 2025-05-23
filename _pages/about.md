---
permalink: /
title: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

Biography
======

Kenneth is currently a Ph.D. student in Electrical and Computer Engineering at Purdue University. He is fortunate to be advised by Professor [Murat Kocaoglu](https://www.muratkocaoglu.com/). His research focuses on causal discovery and its applications to machine learning, especially on invariant prediction and root cause analysis of failure in microservices. He has earned his bachelor's degree in Computer Science and Mathematics from Brigham Young University-Hawaii and his Master's degree in Statistics from UC Davis. He has won best reviewer awards from AISTATS, UAI, and ICLR. He has completed several internships at Newday Investing, Bayer, Experian DataLabs, Genentech, and Amazon.


## 📰 News

{% for item in site.data.news %}
- **{{ item.date | date: "%b %Y" }}**: {{ item.description }}
{% endfor %}


## 📝 Publications

{% assign pubs = site.publications | sort: "date" | reverse %}
{% for pub in pubs limit:4 %}
- **{{ pub.title }}**, *{{ pub.venue }}*, {{ pub.date | date: "%Y" }}.  
  {% if pub.paperurl %}[[paper]({{ pub.paperurl }})]{% endif %}
  {% if pub.codeurl %} [[code]({{ pub.codeurl }})]{% endif %}
{% endfor %}