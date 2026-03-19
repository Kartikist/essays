---
layout: default
title: Essays by Tags
permalink: /tags/
---

# <strong>Essays by Tags</strong>

Browse all essays grouped by topic. Click tags to filter.

{% capture tags %}
  {% for tag in site.tags %}
    {{ tag[0] | replace: '-', ' ' | append: ' (' | append: site.tags[tag[0]].size | append: ')' }}
  {% endfor %}
{% endcapture %}

{% assign sortedtags = tags | split: ' ' | sort %}

<ul style="list-style: none; padding: 0; columns: 2;">
  {% for tag in site.tags %}
  <li style="margin-bottom: 1rem;">
    <a href="#{{ tag[0] | slugify }}" style="font-weight: 700; font-size: 1.2rem; color: #007acc;">
      #{{ tag[0] | replace: '-', ' ' }} ({{ tag[1].size }})
    </a>
    <ul style="margin-top: 0.5rem; padding-left: 1.5rem;">
      {% for post in tag[1] %}
        <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
      {% endfor %}
    </ul>
  </li>
  {% endfor %}
</ul>

<p><a href="/" style="font-weight: 600;">← Back to All Essays</a></p>
