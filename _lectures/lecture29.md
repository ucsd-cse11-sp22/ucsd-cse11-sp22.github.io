---
layout: with-sidebar
index: 29
name: AUA and Goodbye!
released-on: "2022-06-03"
worksheets:
  - title: 9AM Lecture (A00)
    url: https://drive.google.com/file/d/1KgHeQRBvQX54URu8v-rdemaet3qgE_y1
  - title: 10AM Lecture (B00)
    url: https://drive.google.com/file/d/1KypPpa87Ak4mygI7iL5oV-IBLYW9WGSD
---

## Problem Session {{ page.index }} – {{ page.name }}

_{{ page.released-on }}_

Please submit your CAPEs for the course at [https://cape.ucsd.edu/](https://cape.ucsd.edu/), including evaluations for your TAs!

The theme of this lecture is “Ask Us (Almost) Anything!” Feel free to ask questions about the course, CSE, our experience, programming, and so on. This can be a mix of review and other topics you find helpful. 

## Completed Worksheets from Lecture

{% for worksheet in page.worksheets %}
<div class="worksheetBox">
{{ worksheet.title }}
<br>
<iframe src="{{ worksheet.url }}/preview" width="256" height="192" allow="autoplay"></iframe>
</div>
{% endfor %}