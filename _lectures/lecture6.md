---
layout: with-sidebar
index: 6
name: Classes and Objects
released-on: "2022-4-8"
videos:
  - title: Creating Objects and Classes (through 22:00)
    url: https://drive.google.com/file/d/1Kn6rVGCTQf2OkZ5-maVpA-MXFd0LHxZ2
  - title: Point add() Method 1
    url: https://drive.google.com/file/d/1PV8W3eaBZbOab42mzne7Wts_kwEuz6ZU
  - title: Point add() Method 2
    url: https://drive.google.com/file/d/1yZX5wo3b-A5AxOwSIccQqsUR3VK0j26i
  - title: Math methods
    url: https://drive.google.com/file/d/1-5P1JWdzCCfGpwh1aW7jLYApipzJgmKc

worksheets:
  - title: 9AM Lecture (A00)
    url: https://drive.google.com/file/d/18pVqYPaJwJeWsiKmMfRiY7t1XnoBGZ5-
  - title: 10AM Lecture (B00)
    url: https://drive.google.com/file/d/18b3mO7KVoPREpexIAOApLKD3awOOieZs
---

## Problem Session 6 – Classes and Constructors

_{{ page.released-on }}_

Readings to be completed **before** problem session.

- Stepik Chapter 5 [https://stepik.org/lesson/573908/step/1?unit=568498](https://stepik.org/lesson/573908/step/1?unit=568498)

Videos (to watch **before** your problem session on April 8):

{% for video in page.videos %}
[{{ video.title }}]({{ video.url }}){:target="_blank"}

<iframe src="{{ video.url }}/preview" width="640" height="480" allow="autoplay"></iframe>
{% endfor %}

Handout:

<iframe src="https://drive.google.com/file/d/1hY2zSmahlGeYhdXlmlN2nhDez5rwYsYx/preview" width="640" height="480" allow="autoplay"></iframe>

## Completed Worksheets from Lecture

{% for worksheet in page.worksheets %}
<div class="worksheetBox">
{{ worksheet.title }}
<br>
<iframe src="{{ worksheet.url }}/preview" width="256" height="192" allow="autoplay"></iframe>
</div>
{% endfor %}