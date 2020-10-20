---
layout: default
---
# My motorcycle albums

{% assign photo_pages = site.pages %}
{% for photo_page in photo_pages %}
{% if photo_page.url != '/' %}
<h2>{{ photo_page.title }}</h2>
<a href="{{ photo_page.url | prepend: site.baseurl }}">
    <img src="{{photo_page.photo}}" width="300">
</a>
<br/>
{% endif %}
{% endfor %}