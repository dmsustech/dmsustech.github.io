---
layout: default2
title: SUSTech Discrete Mathematics Seminar
---

## Organizers

The SUSTech Discrete Mathematics Seminar is organized by [Ferdinand Ihringer](http://math.ihringer.org), [Caiheng Li](https://www.sustech.edu.cn/en/faculties/licaiheng.html), [Qing Xiang](https://www.sustech.edu.cn/en/faculties/xiangqing.html), and [Ziqing Xiang](http://www.ziqing.org).

You can contact us under [discretemath@sustech.edu.cn](mailto:discretemath@sustech.edu.cn).

For Zoom links, please ask for the password.

## Talks

{% assign tolistpre = site.posts | group_by: "date" %}
{% assign tolist = tolistpre | sort: "time" %}
{% for post in tolist %}
{% if post.show %}
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
