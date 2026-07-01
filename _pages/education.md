---
layout: page
permalink: /education/
title: Education
description: Academic background and degrees.
nav: true
nav_order: 4
---

{% assign education = site.data.cv.cv.sections.Education %}

<div class="education">

{% for edu in education %}

### {% if edu.url %}<a href="{{ edu.url }}">{% endif %}{{ edu.institution }}{% if edu.url %}</a>{% endif %}

**{{ edu.studyType }}** in {{ edu.area }}{% if edu.location %}, {{ edu.location }}{% endif %}

{% if edu.start_date or edu.end_date %}
{{ edu.start_date }}{% if edu.end_date %} – {{ edu.end_date }}{% endif %}
{% endif %}

{% if edu.courses %}
Courses: {{ edu.courses }}
{% endif %}

{% if edu.highlights %}
{% for highlight in edu.highlights %}
- {{ highlight }}
{% endfor %}
{% endif %}

{% endfor %}

</div>
