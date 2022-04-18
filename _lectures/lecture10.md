---
layout: with-sidebar
index: 10
name: Interfaces
released-on: "2022-4-18"
videos:
  - title: Interfaces (watch through 30:00)
    url: https://drive.google.com/file/d/1FsiNPr6N5yiFymHtwCdDHYHt03mWNw_Q
worksheets:
  - title: 9AM Lecture (A00)
    url: https://drive.google.com/file/d/1JZGt_-lU7C_899uIl5NY3qHR3azwFzpX
  - title: 10AM Lecture (B00)
    url: https://drive.google.com/file/d/1J_0ouyfrbJ9uS_FoDO1VLytgMI-VoonV
---

## Problem Session {{ page.index }} – {{ page.name }}

_{{ page.released-on }}_

## Pre-Reading and Videos

Stepik reading:
- [Stepik 8.1-8.3](https://stepik.org/lesson/574307/step/1?unit=568892)

{% for video in page.videos %}
[{{ video.title }}]({{ video.url }}){:target="_blank"}

<iframe src="{{ video.url }}/preview" width="640" height="480" allow="autoplay"></iframe>
{% endfor %}

## Handout

<iframe src="https://drive.google.com/file/d/1nUCwjiK6tzwEyRciOayfLks_7hh-Hfxs/preview" width="640" height="480" allow="autoplay"></iframe>

## Completed Worksheets from Lecture

{% for worksheet in page.worksheets %}
<div class="worksheetBox">
{{ worksheet.title }}
<br>
<iframe src="{{ worksheet.url }}/preview" width="256" height="192" allow="autoplay"></iframe>
</div>
{% endfor %}