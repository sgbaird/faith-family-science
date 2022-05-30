---
layout: page
title: Blog Archive
---

{% for tag in site.tags reversed %}
  <h3>{{ tag[0] }}</h3>
  <ul>
    {% for post in tag[1] reversed %}
      <li><a href="{{ post.url }}">{{ post.date | date: "%B %Y" }} - {{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}