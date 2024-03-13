---
layout: default2
title: SUSTech Discrete Mathematics Seminar
---

## Past Talks

{% assign tolist = site.posts | sort: "date" | reverse %}
{% assign curDate = site.time | date: '%s' %}
{% for post in tolist %}
{% assign postStartDate = post.date | date: '%s' %}
{% if post.show and curDate >= postStartDate %}
<article>

<h2><a href="{{ post.url }}">{{ post.title }}</a></h2>

<p class="view">
{% if post.homepage %}
<strong>Speaker:</strong> <a href="{{post.homepage}}">{{ post.speaker }}</a> ({{ post.affiliation }})<br>
{% else %}
<strong>Speaker:</strong> {{ post.speaker }} ({{ post.affiliation }})<br>
{% endif %}
<strong>Room:</strong> {{ post.place }}<br>
<strong>Time:</strong> {{ post.date | date: '%Y/%m/%d, %A'}}, {{ post.time}}
{% if post.zoom %}
<br>
<strong>Zoom:</strong> <a href="https://us06web.zoom.us/j/{{post.zoomid}}">{{ page.zoomid }}</a>
{% endif %}
</p>

{{post.content}}

</article>
{% endif %}
{% endfor %}
