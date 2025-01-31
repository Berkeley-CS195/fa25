---
layout: page
title: Home
description: Listing of course modules and topics.
nav_order: 1
---

# CS 195: Social Implications of Computer Technology

{: .mb-2 }

## UC Berkeley, Spring 2025
{: .mb-2 .fs-6 .text-grey-dk-000 }

<!-- Insert Buttons here Later -->

<div class="role flex">
  {% assign instructors = site.staffers | where: 'role', 'InstructorHome' %}
  {% for staffer in instructors %}
    {{ staffer }}
  {% endfor %}
</div>


## Schedule

{% assign mods = site.modules | sort: "date" | reverse %}
{% for mod in mods %}
  {% if mod.Status == 'Active' %}
    {{ mod }}
  {% endif %}
{% endfor %}

<script src="{{ '/assets/scripts/announcement-navigation.js' | relative_url }}"></script>
