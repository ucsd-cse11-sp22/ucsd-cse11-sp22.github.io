---
layout: with-sidebar
index: 29
name: A Big Example
released-on: "2022-06-03"
worksheets:
  
---

## Problem Session {{ page.index }} – {{ page.name }}

_{{ page.released-on }}_

Please submit your CAPEs for the course at [https://cape.ucsd.edu/](https://cape.ucsd.edu/), including evaluations for your TAs!

## Pre-class Tasks

This worked example will serve as a review of most of the topics we've seen in
class so far, including interfaces, `Collections` classes, loops, recursion,
testing, and memory diagrams.

Videos: same as previous lecture

Code from videos:

<script src="https://emgithub.com/embed.js?target=https%3A%2F%2Fgithub.com%2Fucsd-cse11-s20%2F19-AllTogether%2Fblob%2Fmaster%2FFilesystemExamples.java&style=github&showBorder=on&showLineNumbers=on&showFileMeta=on&showCopy=on"></script>

Handout:

<iframe src="https://drive.google.com/file/d/1wBkmYhT0M9pDrUAXX-cGrBp1mdnxJIzU/preview" width="640" height="480" allow="autoplay"></iframe>

## Completed Worksheets from Lecture

{% for worksheet in page.worksheets %}
<div class="worksheetBox">
{{ worksheet.title }}
<br>
<iframe src="{{ worksheet.url }}/preview" width="256" height="192" allow="autoplay"></iframe>
</div>
{% endfor %}