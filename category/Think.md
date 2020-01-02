---
layout: default
title: Think
permalink: /category/Think
icon: th-list
type: page
---

<div class="page clearfix">
  <div class="left">
    <h1>{{page.title}}</h1>
    <hr>
    <ul>
      <h2 id="{{category | first}}">{{category | first}}</h2>
      {% for post in site.categories[page.title] %}
      {% if post.url %}
      <li>
        <time>
          {{ post.date | date:"%F" }} {{ post.date | date: "%a" }}.
        </time>
        <a class="title" href="{{ post.url | prepend: site.url }}">{{ post.title }}</a>
      </li>
      {% endif %}
      {% endfor %}
    </ul>
  </div>
</div>