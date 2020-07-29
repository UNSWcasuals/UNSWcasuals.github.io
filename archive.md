---
layout: page
title: "Our Posts"
permalink: /archive/
---
<ul class="post-list archive">
  {%- for post in site.posts reversed -%}
  <li>
    {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
    <h4 class="post-title">
      <a class="post-link" href="{{ post.url | relative_url }}">
        {{ post.title | escape }}
      </a>
    </h4>
    <span class="post-meta">{{ post.date | date: date_format }}</span>
    {%- if site.show_excerpts -%}
      {{ post.excerpt }}
    {%- endif -%}
  </li>
  {%- endfor -%}
</ul>
