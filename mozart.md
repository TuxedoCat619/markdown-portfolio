---
layout: default
title: "Mozart's Compositions - A YouTube Link Tree"
---

## Mozart's Compositions - A YouTube Link Tree

Welcome! Below is a curated list of some of Mozart's famous compositions with links to YouTube videos.

{% assign compositions_by_category = site.data.mozart_compositions | group_by: "category" %}
{% for category_group in compositions_by_category %}
  <h3>{{ category_group.name }}</h3>
  <ul>
    {% for item in category_group.items %}
      <li><a href="{{ item.youtube_url }}" target="_blank">{{ item.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}
