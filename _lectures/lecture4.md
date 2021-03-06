---
layout: with-sidebar
index: 4
name: String Methods
released-on: "2022-4-4"
videos:
  - title: Strings
    url: https://drive.google.com/file/d/1VFHfgw_tP8snhfDoEhns5ORbJz6UFeDw
  - title: String Concatenation
    url: https://drive.google.com/file/d/14bS8OZyY0oPYFlLCnFHZ6Vz5xAI6jzE8    
  - title: Strings and Numbers
    url: https://drive.google.com/file/d/1NBZa_qDiGO9V6cwWZddtBpNTQzF348oL
  - title: Method Evaluation
    url: https://drive.google.com/file/d/1WScX4N4gFNAlLoHdXwoVurQacUB2X2JF
  - title: String Methods
    url: https://drive.google.com/file/d/1WnSDBSOGSXnsvAvgdYduFYzuS9RTIscK

worksheets:
  - title: 9AM Lecture (A00)
    url: https://drive.google.com/file/d/136UarTqzPwONQU7W5Fja8BSYQgByo5W9
  - title: 10AM Lecture (B00)
    url: https://drive.google.com/file/d/13K6RQ6Cfm5K8SPcOWhGeHEgLbJ4VZxpC
---

## Problem Session 4 – Strings and More Methods 

_{{ page.released-on }}_

Readings (to be completed by 9am on April 4, **before** problem session). 

- No Stepik readings for this lecture

Videos (to watch **before** your problem session on April 4):

{% for video in page.videos %}
[{{ video.title }}]({{ video.url }}){:target="_blank"}

<iframe src="{{ video.url }}/preview" width="640" height="480" allow="autoplay"></iframe>
{% endfor %}

Handout

<iframe src="https://drive.google.com/file/d/1hRvp-vspBMLX9GFSKYZkF0iSvvdsMLjZ/preview" width="640" height="480" allow="autoplay"></iframe>

## Completed Worksheets from Lecture

{% for worksheet in page.worksheets %}
<div class="worksheetBox">
{{ worksheet.title }}
<br>
<iframe src="{{ worksheet.url }}/preview" width="256" height="192" allow="autoplay"></iframe>
</div>
{% endfor %}
