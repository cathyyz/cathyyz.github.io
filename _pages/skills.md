---
layout: page
permalink: /skills/
title: Skills
description: Technical and professional skills.
nav: true
nav_order: 3
---

{% assign skills = site.data.cv.cv.sections.Skills %}

<div class="skills">

{% for skill in skills %}

### {{ skill.name }}{% if skill.level %} ({{ skill.level }}){% endif %}

{% if skill.icon %}<i class="{{ skill.icon }}"></i>{% endif %}

{% if skill.keywords %}
{{ skill.keywords }}
{% endif %}

{% endfor %}

</div>
