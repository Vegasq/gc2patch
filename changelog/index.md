---
layout: default
title: Changelog
---

<div class="changelog-index">

# Changelog

<ul class="changelog-list">
{% for post in site.posts %}
  <li class="changelog-entry">
    <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
    <div class="meta">
      <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %d, %Y" }}</time>
      {% if post.version %}<span class="version">v{{ post.version }}</span>{% endif %}
    </div>
    {% if post.excerpt %}
    <p class="excerpt">{{ post.excerpt | strip_html | truncate: 200 }}</p>
    {% endif %}
    <a href="{{ post.url | relative_url }}" class="read-more">Read more &rarr;</a>
  </li>
{% endfor %}
</ul>

</div>
