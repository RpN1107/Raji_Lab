---
title: Team
nav:
  order: 3
  tooltip: Meet our team
---

# {% include icon.html icon="fa-solid fa-users" %} Team

Our lab brings together researchers from computational biology, biophysics, molecular simulations, and bioinformatics to study intrinsically disordered proteins and biomolecular dynamics.

{% include section.html %}

{% assign pi_members = site.members | where: "role", "pi" %}
{% assign phd_members = site.members | where: "role", "phd" | sort: "start_year" %}
{% assign alumni_members = site.members | where: "role", "alumni" | sort: "end_year" | reverse %}

## Principal Investigator

{% for member in pi_members %}

<div class="member-entry" style="margin-bottom: 3rem;">

<img src="{{ member.image | relative_url }}" width="220">

### {{ member.name }}

**Role:** Principal Investigator

{{ member.description }}

[View Profile]({{ member.url | relative_url }})

</div>

{% endfor %}

---

## PhD Students

{% for member in phd_members %}

<div class="member-entry" style="margin-bottom: 3rem;">

<img src="{{ member.image | relative_url }}" width="200">

### {{ member.name }}

**Started:** {{ member.start_year }}

{{ member.description }}

[View Profile]({{ member.url | relative_url }})

</div>

{% endfor %}

---

## Previous Students

<div style="display: flex; flex-direction: column; gap: 1.5rem;">

{% for member in alumni_members %}

<div style="display: flex; align-items: center; gap: 1rem;">

<img 
  src="{{ member.image | relative_url }}" 
  width="70" 
  height="70"
  style="border-radius: 50%; object-fit: cover;"
>

<div>

### {{ member.name }}

**Years:** {{ member.start_year }} – {{ member.end_year }}

**Current Affiliation:** {{ member.current_affiliation }}

</div>

</div>

{% endfor %}

</div>

{% include section.html %}
