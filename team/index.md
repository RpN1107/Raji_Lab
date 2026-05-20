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
{% assign phd_members = site.members | where: "role", "phd" | sort: "start_order" %}
{% assign alumni_members = site.members | where: "role", "alumni" | sort: "start_order" | reverse %}

## Principal Investigator

{% for member in pi_members %}

<div class="member-entry" style="margin-bottom: 3rem;">

  <img 
    src="{{ member.image | relative_url }}" 
    width="220"
    style="border-radius: 12px; object-fit: cover;"
  >

  <h3>{{ member.name }}</h3>

  <p>
    <strong>Role:</strong> Principal Investigator
  </p>

  <p>
    {{ member.description }}
  </p>

  <p>
    <a href="{{ member.url | relative_url }}">
      View Profile
    </a>
  </p>

</div>

{% endfor %}

---

## PhD Students

{% for member in phd_members %}

<div class="member-entry" style="margin-bottom: 3rem;">

  <img 
    src="{{ member.image | relative_url }}" 
    width="200"
    style="border-radius: 12px; object-fit: cover;"
  >

  <h3>{{ member.name }}</h3>

  <p>
    <strong>Duration:</strong> {{ member.duration }}
  </p>

  <p>
    {{ member.description }}
  </p>

  <p>
    <a href="{{ member.url | relative_url }}">
      View Profile
    </a>
  </p>

</div>

{% endfor %}

---

## Previous Students

<div style="display: flex; flex-direction: column; gap: 2rem;">

{% for member in alumni_members %}

<div style="display: flex; align-items: center; gap: 1rem;">

  <img 
    src="{{ member.image | relative_url }}" 
    width="70" 
    height="70"
    style="border-radius: 50%; object-fit: cover;"
  >

  <div>

    <h3 style="margin-bottom: 0.3rem;">
      {{ member.name }}
    </h3>

    <p style="margin: 0;">
      <strong>Duration:</strong> {{ member.duration }}
    </p>

    <p style="margin: 0;">
      <strong>Current Affiliation:</strong> {{ member.current_affiliation }}
    </p>

  </div>

</div>

{% endfor %}

</div>

{% include section.html %}
