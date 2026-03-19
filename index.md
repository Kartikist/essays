---
layout: default
title: Home
permalink: /
---

## <strong>All Essays</strong>

{% if site.posts.size > 0 %}
<ul class="post-list">
  {% for post in site.posts limit: 100 %}
  <li>
    <a href="{{ post.url | relative_url }}" class="post-title">{{ post.title }}</a>
    <div class="post-meta">
      {% if post.tags.size > 0 %}
        Tags: {% for tag in post.tags %}<strong>#{{ tag }}</strong>{% unless forloop.last %}, {% endunless %}{% endfor %}
      {% endif %}
    </div>
    {% if post.excerpt %}
      <div class="post-excerpt">{{ post.excerpt | strip_html | truncatewords: 30 }}</div>
    {% endif %}
  </li>
  {% endfor %}
</ul>
{% else %}
<p><strong>No essays yet—add some to <code>_posts/</code>!</strong></p>
{% endif %}
