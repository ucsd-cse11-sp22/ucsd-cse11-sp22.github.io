---
layout: with-sidebar
index: 9
name: Nested Data
released-on: "2022-4-15"
worksheets:
  - title: Lecture
    url: https://drive.google.com/file/d/1oyCqo-zFgz6VqUOuoneyqcsvb5SYdtMy
---

## Problem Session {{ page.index }} – {{ page.name }}

_{{ page.released-on }}_

Due to the early release of the exam, there will be no in-person lecture on Friday, April 15.

Watch the Lecture Video Recording (From Winter 2022) and do the handouts on your own. You can find the video
recording at the bottom of this page.

Stepik reading (to complete before class on April 15):
- [Stepik 7](https://stepik.org/lesson/584041/step/10?unit=578810)

No pre-watch videos for April 15 (take the time to review some others!).

If you want to watch ahead, the next topic will be from here, but we won't
discuss interfaces until the next class:

<iframe src="https://drive.google.com/file/d/1FsiNPr6N5yiFymHtwCdDHYHt03mWNw_Q/preview" width="640" height="480" allow="autoplay"></iframe>

Handout:

<iframe src="https://drive.google.com/file/d/1n7L9htMXqHneP0HFahuxucobzNIgR-kd/preview" width="640" height="480" allow="autoplay"></iframe>

## Lecture Video Recording (From Winter 2022)

[Lecture 9 - Recording](https://drive.google.com/file/d/1oXd7SkEuVPBdWZR7tg9hoCu3TmJoYPhJ){:target="_blank"}

<iframe src="https://drive.google.com/file/d/1oXd7SkEuVPBdWZR7tg9hoCu3TmJoYPhJ/preview" width="640" height="480" allow="autoplay"></iframe>

## Completed Worksheets from Lecture

{% for worksheet in page.worksheets %}
<div class="worksheetBox">
{{ worksheet.title }}
<br>
<iframe src="{{ worksheet.url }}/preview" width="256" height="192" allow="autoplay"></iframe>
</div>
{% endfor %}