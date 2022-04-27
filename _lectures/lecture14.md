---
layout: with-sidebar
index: 14
name: Variables and Loops
released-on: "2022-4-27"
videos:
  - title: Variable Update
    url: https://drive.google.com/file/d/1BXvDBZyKMf-L3ET3cBFcmB-V7b4Et7yf
  - title: Variable Update Examples
    url: https://drive.google.com/file/d/1Dh3eJqLtE3_kCP-28fMayK07UWgy-7Xp
  - title: Loops
    url: https://drive.google.com/file/d/1At2ogDjHBMuE9Ci-tHwcdSqY8xx5I3r1
  - title: Loops Examples
    url: https://drive.google.com/file/d/1BwyC-9QP85-SX3VlSPkbNfWxjrmTd4dT
worksheets:
  - title: 9AM Lecture (A00)
    url: https://drive.google.com/file/d/1QIFPuPR3ZMPWre_hvI5BtJfXFErMgcMj
  - title: 10AM Lecture (B00)
    url: https://drive.google.com/file/d/1QoAKRbUrTlRAKfCgteWBE880y9AIxL4R
---

## Problem Session {{ page.index }} – {{ page.name }}

_{{ page.released-on }}_

## Pre-Reading and Videos

Stepik reading:
- [Stepik 10](https://stepik.org/lesson/579629/step/1?unit=574279)

{% for video in page.videos %}
[{{ video.title }}]({{ video.url }}){:target="_blank"}

<iframe src="{{ video.url }}/preview" width="640" height="480" allow="autoplay"></iframe>
{% endfor %}

## Handout

<iframe src="https://drive.google.com/file/d/1teCdQVzzKBV9syE9p0rQj53UcTAyRjOm/preview" width="640" height="480" allow="autoplay"></iframe>

## Completed Worksheets from Lecture

{% for worksheet in page.worksheets %}
<div class="worksheetBox">
{{ worksheet.title }}
<br>
<iframe src="{{ worksheet.url }}/preview" width="256" height="192" allow="autoplay"></iframe>
</div>
{% endfor %}