---
layout: page
permalink: /contact/
title: Contact
description: Get in touch.
nav: true
nav_order: 6
---

<div id="contact" class="contact">

{{ site.contact_note }}

{% if site.data.socials.email %}
**Email:** [{{ site.data.socials.email }}](mailto:{{ site.data.socials.email }})
{% endif %}

</div>
