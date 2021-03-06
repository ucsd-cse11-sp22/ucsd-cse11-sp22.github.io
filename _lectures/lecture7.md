---
layout: with-sidebar
index: 7
name: Memory and Tracing
released-on: "2022-4-11"
videos:
  - title: Creating Objects and Classes (22:00 - 38:00)
    url: https://drive.google.com/file/d/1Kn6rVGCTQf2OkZ5-maVpA-MXFd0LHxZ2
  - title: Line Class
    url: https://drive.google.com/file/d/1bFzLGW75Y68hAEVe3ERDvdQf7jHJ0Kin
  - title: Calc-Y
    url: https://drive.google.com/file/d/1WSf8sB8OZOz8Y4O8x7l4qKLP4McYIqo7

worksheets:
  - title: 9AM Lecture (A00)
    url:  https://drive.google.com/file/d/19satqAnmbFiHcjHbu93ipYLRtqJwfB0n
  - title: 10AM Lecture (B00)
    url: https://drive.google.com/file/d/19svW0OWw8Mpa7uuFA2CBvaL3UGCjnVRK
---

## Problem Session {{ page.index }} – {{ page.name }}

_{{ page.released-on }}_

No Stepik readings for Monday.

{% for video in page.videos %}
[{{ video.title }}]({{ video.url }}){:target="_blank"}

<iframe src="{{ video.url }}/preview" width="640" height="480" allow="autoplay"></iframe>
{% endfor %}

Handout:

<iframe src="https://drive.google.com/file/d/1logfnUobeyKbuN5wHqP2tpAv1awzbwXr/preview" width="640" height="480" allow="autoplay"></iframe>

## Completed Worksheets from Lecture

{% for worksheet in page.worksheets %}
<div class="worksheetBox">
{{ worksheet.title }}
<br>
<iframe src="{{ worksheet.url }}/preview" width="256" height="192" allow="autoplay"></iframe>
</div>
{% endfor %}