---
layout: with-sidebar
index: 27
name: Modifiers, Invariants
released-on: "2022-05-27"
videos:
    - title: "Access Modifiers"
      url: https://drive.google.com/file/d/1j8xtQfJtdHfBDp_4eINFE7xYg2IUEs7g
    - title: "Default Package"
      url: https://drive.google.com/file/d/1jIgflYWbjJdfdRz5Kh0LTLBSP54nnlbM
    - title: "Protected"
      url: https://drive.google.com/file/d/1-2lleGWYeeXkiTaRmWbTtOeM3lZ7uHSP
worksheets:
  - title: 9AM Lecture (A00)
    url: https://drive.google.com/file/d/1CqkwWdXy3QWM8ceR6f2IwnjHLJcLZ7yO
  - title: 10AM Lecture (B00)
    url: https://drive.google.com/file/d/1Cn69Rsa5efSBShQkj0p_YTzvurI6YApO
---

## Problem Session {{ page.index }} – {{ page.name }}

_{{ page.released-on }}_

## Pre-class Tasks

[Stepik 13](https://stepik.org/lesson/575460/step/1?unit=570041) (Abstract Classes)

Videos:

{% for video in page.videos %}
[{{ video.title }}]({{ video.url }}){:target="_blank"}
<iframe src="{{ video.url }}/preview" width="640" height="480" allow="autoplay"></iframe>
{% endfor %}

## Handout

<iframe src="https://drive.google.com/file/d/1wQR7W3phH3nHf-b7bw0aAQX-m1Va0et4/preview" width="640" height="480" allow="autoplay"></iframe>

## Completed Worksheets from Lecture

{% for worksheet in page.worksheets %}
<div class="worksheetBox">
{{ worksheet.title }}
<br>
<iframe src="{{ worksheet.url }}/preview" width="256" height="192" allow="autoplay"></iframe>
</div>
{% endfor %}