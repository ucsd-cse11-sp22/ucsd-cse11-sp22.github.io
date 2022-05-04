---
layout: with-sidebar
index: 17
name: Nested Loops
released-on: "2022-5-4"
videos:
  - title: Nested Loops
    url: https://drive.google.com/file/d/1tV46H_TBDBQkS04_kfQHGJbhRA70n8Gs
  - title: Region Loop
    url: https://drive.google.com/file/d/157v75MQE_k0h-z9S3_tCVvaHIP-nvWFs
worksheets:
  - title: 9AM Lecture (A00)
    url: https://drive.google.com/file/d/1XVVkx6P-VgV3Mk8IrC0exMQC6zIZ9iRF
  - title: 10AM Lecture (B00)
    url: https://drive.google.com/file/d/1XXYQz3ZMbaE1WA8473Mlx4XZnV-5vA19
---

## Problem Session {{ page.index }} – {{ page.name }}

_{{ page.released-on }}_

## Pre-class Tasks

Stepik 11.1 [https://stepik.org/lesson/609849/step/1?unit=605131](https://stepik.org/lesson/609849/step/1?unit=605131)

{% for video in page.videos %}
[{{ video.title }}]({{ video.url }}){:target="_blank"}

<iframe src="{{ video.url }}/preview" width="640" height="480" allow="autoplay"></iframe>
{% endfor %}

## Handout

Same as last lecture (the `main` part)

<iframe src="https://drive.google.com/file/d/1vpoDLspl4rsQGHkEinrRD1NJQ8K1np_j/preview" width="640" height="480" allow="autoplay"></iframe>

## Completed Worksheets from Lecture

{% for worksheet in page.worksheets %}
<div class="worksheetBox">
{{ worksheet.title }}
<br>
<iframe src="{{ worksheet.url }}/preview" width="256" height="192" allow="autoplay"></iframe>
</div>
{% endfor %}