---
layout: with-sidebar
index: 16
name: Loops and Objects
released-on: "2022-5-2"
videos:
  - title: Factorial, Twice
    url: https://drive.google.com/file/d/1knoFKHlFXGgDHrkJzYfdxtX6mJLcivPY
  - title: Factorial, Compared
    url: https://drive.google.com/file/d/16opUdYNITHGgW9X6F_KGoBmALhCWwZZx
  - title: Arrays of References
    url: https://drive.google.com/file/d/12ZjQNBxnWpthOJt1tZ8YMonLzXQ7XzCT
  - title: Methods on Arrays of References
    url: https://drive.google.com/file/d/1TdAj2ypxk43s1LWmJ2HEtBb_vGTokFuR
  - title: More Methods on Arrays of References
    url: https://drive.google.com/file/d/1wx4xHmkzH8G6L2NoMZU6Gff8gtqA9xGY
worksheets:
  - title: 9AM Lecture (A00)
    url: https://drive.google.com/file/d/1WQjMSjqttkTVIo83yySYFvrhmG82KUtI
  - title: 10AM Lecture (B00)
    url: https://drive.google.com/file/d/1WiKB8VRd5F0BeafOvoyiM1T5K7jW5N7o
---

## Problem Session {{ page.index }} – {{ page.name }}

_{{ page.released-on }}_

## Pre-class Tasks

No new Stepik reading.

{% for video in page.videos %}
[{{ video.title }}]({{ video.url }}){:target="_blank"}
<iframe src="{{ video.url }}/preview" width="640" height="480" allow="autoplay"></iframe>
{% endfor %}

## Handout

<iframe src="https://drive.google.com/file/d/1vpoDLspl4rsQGHkEinrRD1NJQ8K1np_j/preview" width="640" height="480" allow="autoplay"></iframe>

## Completed Worksheets from Lecture

{% for worksheet in page.worksheets %}
<div class="worksheetBox">
{{ worksheet.title }}
<br>
<iframe src="{{ worksheet.url }}/preview" width="256" height="192" allow="autoplay"></iframe>
</div>
{% endfor %}