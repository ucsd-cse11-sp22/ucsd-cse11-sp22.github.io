---
layout: with-sidebar
index: 19
name: Connect 4!
released-on: "2022-05-09"
videos:
worksheets:
  - title: 9AM Lecture (A00)
    url: https://drive.google.com/file/d/1ffSECmdyrpqIzO41gFr8_UTW7iBIJABN
  - title: 10AM Lecture (B00)
    url: https://drive.google.com/file/d/1ffoA8heYdFRq_tm2Z4aTCecAU-DN7eZF
---

## Problem Session {{ page.index }} – {{ page.name }}

_{{ page.released-on }}_

No new content for pre-class; we'll work through the Connect 4 example more
today.

## Handout

<iframe src="https://drive.google.com/file/d/1vyAaXbHgsHagaOgrKHeFKOVarL3FMM-M/preview" width="640" height="480" allow="autoplay"></iframe>

## Completed Worksheets from Lecture

{% for worksheet in page.worksheets %}
<div class="worksheetBox">
{{ worksheet.title }}
<br>
<iframe src="{{ worksheet.url }}/preview" width="256" height="192" allow="autoplay"></iframe>
</div>
{% endfor %}