---
layout: default2
---

## Organizers

The SUSTech Discrete Mathematics Seminar is organized by [Ferdinand Ihringer](http://math.ihringer.org), [Caiheng Li](https://www.sustech.edu.cn/en/faculties/licaiheng.html), [Qing Xiang](https://www.sustech.edu.cn/en/faculties/xiangqing.html), and [Ziqing Xiang](http://www.ziqing.org).

You can contact us under [discretemath@sustech.edu.cn](mailto:discretemath@sustech.edu.cn).

For Zoom links, please ask for the password.

## Talks

  {% for post in site.posts %}
  <article>

<h2><a href="{{ post.url }}">{{ post.title }}</a></h2>

<p class="view">
<strong>Speaker:</strong> {{ post.speaker | default: site.author }} ({{ post.affiliation }})<br>
<strong>Room:</strong> {{ post.place }}<br>
<strong>Time:</strong> {{ post.time}} <br>
<strong>Zoom:</strong> <a href="https://us06web.zoom.us/j/{{post.zoomid}}">{{ post.zoomid }}</a> 
</p>

{{post.content}}




  </article>
{% endfor %}

