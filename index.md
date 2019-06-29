---
layout: page
title: John M. Mola
subtitle: Bee biology, pollination ecology, population genetics
css: "/css/index.css"
meta-title: "John M. Mola"
meta-description: "PhD Candidate in Ecology at the University of California Davis"
bigimg:
  - "/img/big/DSCN1710.png" : "Bombus vosnesenskii visiting Penstemon rydbergii. Truckee, CA. 2015"
  - "/img/big/DSCN0208.png" : "Blue orchard bee in experimental block. Blue Lake, CA. 2015"
  - "/img/big/DSCN1765_2.png" : "Bombus vosnesenskii on mountain pennyroyal. Truckee, CA. 2015"
  - "/img/big/DSCN2027.png" : "Capturing queen bumble bees. Mclaughlin Reserve. 2016"
  - "/img/big/DSCN2065.png" : "Post-fire bloom of Trifolium fucatum and supporting cast. McLaughlin Reserve. 2015"

---



<div style="text-align:center">
  <p style="font-family: calibri; font-size:22pt">
  PhD Candidate, <a href="http://williamslab.ucdavis.edu">Williams Lab</a> <br>
  Graduate Group in Ecology <br>
  University of California Davis <br>
  johnmmola [at] gmail.com
  
  </p>
</div>

---

<div class="posts-list">
  {% for post in site.posts limit:5 %}
  <article class="post-preview">
    <a href="{{ post.url | prepend: site.baseurl }}">
      <h2 class="post-title">{{ post.title }}</h2>

      {% if post.subtitle %}
      <h3 class="post-subtitle">
        {{ post.subtitle }}
      </h3>
      {% endif %}
    </a>

    <p class="post-meta">
      Posted on {{ post.date | date: "%B %-d, %Y" }}
    </p>

    <div class="post-entry-container">
      {% if post.image %}
      <div class="post-image">
        <a href="{{ post.url | prepend: site.baseurl }}">
          <img src="{{ post.image }}">
        </a>
      </div>
      {% endif %}
      <div class="post-entry">
        {{ post.excerpt | strip_html | xml_escape | truncatewords: site.excerpt_length }}
        {% assign excerpt_word_count = post.excerpt | number_of_words %}
        {% if post.content != post.excerpt or excerpt_word_count > site.excerpt_length %}
          <a href="{{ post.url | prepend: site.baseurl }}" class="post-read-more">[Read&nbsp;More]</a>
        {% endif %}
      </div>
    </div>

    {% if post.tags.size > 0 %}
    <div class="blog-tags">
      Tags:
      {% if site.link-tags %}
      {% for tag in post.tags %}
      <a href="{{ site.baseurl }}/tags#{{ tag }}">{{ tag }}</a>
      {% endfor %}
      {% else %}
        {{ post.tags | join: ", " }}
      {% endif %}
    </div>
    {% endif %}

   </article>
  {% endfor %}
</div>

---
<p align="center">

<a class="twitter-timeline" data-height="800" data-width="400" data-theme="light" data-link-color="#FAB81E" href="https://twitter.com/_JohnMola?ref_src=twsrc%5Etfw">Tweets by _JohnMola</a> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>
</p>