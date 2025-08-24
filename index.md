---
layout: default
title: "Home"
permalink: "/"
---

<section id="about">
  <h2>About</h2>
  <p>
    I am Jong-eun Baek, a Master’s student in the <a href="https://sailab.kaist.ac.kr/" target="_blank" rel="noopener noreferrer">SAIL</a>ab at the Kim Jaechul Graduate School of AI, KAIST, advised by Prof. Jaesik Choi.
  </p>
  <p>
    I received my B.S. in Computer Science and Engineering from POSTECH and studied abroad at RWTH Aachen University as an exchange student.
  </p>
  <p>
    My research interests lie in Natural Language Processing (NLP) and Explainable AI (XAI), with a particular focus on uncovering the causes of hallucination in large language models and investigating how knowledge is represented and stored within them. My ultimate goal is to make language models reliable—systems that explain knowledge in a user-adapted way and provide faithful, explainable outputs.
  </p>
</section>

<section id="news">
  <h2>News</h2>
  <ul class="news">
    {% assign items = site.data.news | sort: "date" | reverse %}
    {% for n in items %}
      <li><span class="news-date">{{ n.date }}</span> — <span class="news-text">{{ n.text }}</span></li>
    {% endfor %}
  </ul>
</section>

<section id="publications">
  <h2>Publications</h2>
  {% assign years = site.data.publications | keys | sort | reverse %}
  {% for y in years %}
    {% assign pubs = site.data.publications[y] %}
    {% if pubs %}
      {% for p in pubs %}
        {% include publication_item.html pub=p me=site.owner_name year=y %}
      {% endfor %}
    {% endif %}
  {% endfor %}
</section>
