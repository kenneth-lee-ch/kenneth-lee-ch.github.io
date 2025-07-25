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

Kenneth is a Ph.D. student in Electrical and Computer Engineering at Purdue University, advised by Professor [Murat Kocaoglu](https://www.muratkocaoglu.com/). His research centers on causal discovery and its applications in machine learning, with a particular focus on invariant prediction and root cause analysis of failures in microservices. He holds a B.S. in Computer Science and Mathematics from Brigham Young University–Hawaii and an M.S. in Statistics from UC Davis. Kenneth has received best reviewer awards from AISTATS, UAI, and ICLR, and has completed internships at Dell EMC, Newday Investing, Bayer, Experian DataLabs, Genentech, and Amazon.


## 📰 News

{% for item in site.data.news %}
- **{{ item.date | date: "%b %Y" }}**: {{ item.description }}
{% endfor %}


## 📝 Publications (<sup>†</sup> indicates equal contribution)

{% assign pubs = site.publications | sort: "date" | reverse %}
{% for pub in pubs %}
<ul>
  <li>
    <strong>{{ pub.title }}</strong>{% if pub.contrib_note %} <small>({{ pub.contrib_note }})</small>{% endif %}<br />
    {{ pub.authors | replace: "K. Lee", "<strong>K. Lee</strong>" }}. <em>{{ pub.venue }}</em>, {{ pub.date | date: "%Y" }}. 
    {% assign links = "" %}
    {% if pub.paperurl %}{% assign links = links | append: '<a href="' | append: pub.paperurl | append: '">[paper]</a> ' %}{% endif %}
    {% if pub.codeurl %}{% assign links = links | append: '<a href="' | append: pub.codeurl | append: '">[code]</a> ' %}{% endif %}
    {% if pub.bibtexurl %}{% assign links = links | append: '<a href="' | append: pub.bibtexurl | append: '">[bibtex]</a>' %}{% endif %}
    <span style="display:inline;">{{ links }}</span>
  </li>
</ul>
{% endfor %}
<!-- ## 📝 Publications (<sup>†</sup> indicates equal contribution)

{% assign pubs = site.publications | sort: "date" | reverse %}
{% for pub in pubs %}
- **{{ pub.title }}**  
  {{ pub.authors | replace: "K. Lee", "**K. Lee**" }}. *{{ pub.venue }}*, {{ pub.date | date: "%Y" }}.  
  {% if pub.paperurl %}[[paper]({{ pub.paperurl }})]{% endif %}
  {% if pub.codeurl %} [[code]({{ pub.codeurl }})]{% endif %}
  {% if pub.slidesurl %}[[paper]({{ pub.slidesurl }})]{% endif %}
  {% if pub.bibtexurl %} [[bibtex]({{ pub.bibtexurl }})]{% endif %}
{% endfor %} -->