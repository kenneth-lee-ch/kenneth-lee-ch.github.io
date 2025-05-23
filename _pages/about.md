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
- **{{ item.date | date: "%b %Y" }}**: {{ item.description | markdownify }}
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
  {% if pub.bibtexurl %} [[bibtex]({{ pub.bibtexurl }})]{% endif %}
{% endfor %} -->