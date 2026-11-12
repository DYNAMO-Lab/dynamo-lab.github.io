---
layout: page
permalink: /news-updates/
title: news
page-title: News & Updates
description: Research highlights, publications, student achievements, and activities from the DYNAMO group.
nav: true
nav_order: 6
---

Research highlights, publications, student achievements, and activities from the DYNAMO group at UC Santa Barbara.

{% assign all_news = site.news | sort: "date" | reverse %}
{% assign current_year = "" %}
{% for item in all_news %}
{% assign y = item.date | date: "%Y" %}
{% if y != current_year %}
## {{ y }}
{% assign current_year = y %}
{% endif %}
{% if item.month_only %}
<h3 id="{{ item.slug }}">{{ item.date | date: "%B %Y" }} — {{ item.title }}</h3>

{{ item.content | markdownify }}
{% else %}
<p><strong>{{ item.date | date: "%B %-d, %Y" }}</strong> — {{ item.content | remove: '<p>' | remove: '</p>' }}</p>
{% endif %}
{% endfor %}
