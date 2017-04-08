---
layout: default
title: "分类：Categories"
---
{% for cat in site.all_categories %}{% if page.category == cat[0] %}<a href="/">首页</a>&nbsp;>&nbsp;<a href="{{cat[2]}}">{{cat[1]}}</a>&nbsp;>&nbsp;列表{% endif %}{% endfor %}
<!-- List -->
<ul class="list-unstyled">
{% for post in site.categories[page.category] %}
  {% capture y %}{{post.date | date:"%Y"}}{% endcapture %}
  {% if year != y %}
	{% assign year = y %}
	<h2>{{ post.date | date: '%Y' }}</h2>
  {% endif %}
  <li>
	<h4><span>{{ post.date | date:"%Y-%m-%d" }}</span>&raquo;
	<a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a></h4>
  </li>
{% endfor %}
