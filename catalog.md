---
layout: page
title: 目錄
---
### 目錄<br><br>

<!-- Posts Title List-->
<ul>

{% for post in site.posts %}
{% if post.pinned %}
<li>
<a href="{% if site.baseurl == '/' %}{{ post.url }}{% else %}{{ post.url | prepend: site.baseurl }}{% endif %}">{{ post.title }}</a>
</li>
{% endif %}
{% endfor %}

{% for post in site.posts %}
{% unless post.pinned %}
<li>
<a href="{% if site.baseurl == '/' %}{{ post.url }}{% else %}{{ post.url | prepend: site.baseurl }}{% endif %}">{{ post.title }}</a>
</li>
{% endunless %}
{% endfor %}

</ul>

<br>
