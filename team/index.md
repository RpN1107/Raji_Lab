```markdown
---
title: Team
nav:
  order: 2
  tooltip: Meet our team
---

# {% include icon.html icon="fa-solid fa-users" %} Team

Our lab brings together researchers from computational biology, biophysics, molecular simulations, and bioinformatics to study intrinsically disordered proteins and biomolecular dynamics.

{% include section.html %}

{% assign pi_members = site.members | where: "role", "pi" %}
{% assign phd_members = site.members | where: "role", "phd" | sort: "start_order" %}
{% assign masters_members = site.members | where: "role", "masters" | sort: "start_order" %}
{% assign alumni_members = site.members | where: "role", "alumni" | sort: "start_order" | reverse %}

## Principal Investigator

<div style="display: flex; justify-content: center; margin-top: 2rem; margin-bottom: 4rem;">

{% for member in pi_members %}

<div style="
display: flex;
flex-direction: column;
align-items: center;
text-align: center;
max-width: 320px;
">

  <a href="{{ member.url | relative_url }}">
    <img
      src="{{ member.image | relative_url }}"
      width="240"
      height="240"
      style="border-radius: 16px; object-fit: cover;"
    >
  </a>

  <h3 style="margin-top: 1rem; margin-bottom: 0.3rem; text-align: center;">
    {{ member.name }}
  </h3>

  <p style="margin: 0; text-align: center;">
    {{ member.position }}
  </p>

  {% if member.duration %}
  <p style="margin-top: 0.2rem; font-style: italic; text-align: center;">
    {{ member.duration }}
  </p>
  {% endif %}

  <p style="margin-top: 0.7rem; text-align: center;">
    {{ member.description }}
  </p>

</div>

{% endfor %}

</div>

---

## PhD Students

<div style="
display: grid;
grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
gap: 3rem;
margin-top: 2rem;
margin-bottom: 4rem;
">

{% for member in phd_members %}

<div style="
display: flex;
flex-direction: column;
align-items: center;
text-align: center;
">

  <a href="{{ member.url | relative_url }}">
    <img
      src="{{ member.image | relative_url }}"
      width="200"
      height="200"
      style="border-radius: 16px; object-fit: cover;"
    >
  </a>

  <h3 style="margin-top: 1rem; margin-bottom: 0.3rem; text-align: center;">
    {{ member.name }}
  </h3>

  <p style="margin: 0; text-align: center;">
    {{ member.position }}
  </p>

  <p style="margin-top: 0.2rem; font-style: italic; text-align: center;">
    {{ member.duration }}
  </p>

  <p style="margin-top: 0.7rem; text-align: center;">
    {{ member.description }}
  </p>

</div>

{% endfor %}

</div>

---

## Master's Students

<div style="
display: grid;
grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
gap: 3rem;
margin-top: 2rem;
margin-bottom: 4rem;
">

{% for member in masters_members %}

<div style="
display: flex;
flex-direction: column;
align-items: center;
text-align: center;
">

  <a href="{{ member.url | relative_url }}">
    <img
      src="{{ member.image | relative_url }}"
      width="200"
      height="200"
      style="border-radius: 16px; object-fit: cover;"
    >
  </a>

  <h3 style="margin-top: 1rem; margin-bottom: 0.3rem; text-align: center;">
    {{ member.name }}
  </h3>

  <p style="margin: 0; text-align: center;">
    {{ member.position }}
  </p>

  <p style="margin-top: 0.2rem; font-style: italic; text-align: center;">
    {{ member.duration }}
  </p>

  <p style="margin-top: 0.7rem; text-align: center;">
    {{ member.description }}
  </p>

</div>

{% endfor %}

</div>

---

## Previous Students

<div style="
display: grid;
grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
gap: 2rem;
margin-top: 2rem;
">

{% for member in alumni_members %}

<div style="
display: flex;
flex-direction: column;
align-items: center;
text-align: center;
">

  <img
    src="{{ member.image | relative_url }}"
    width="120"
    height="120"
    style="border-radius: 50%; object-fit: cover;"
  >

  <h3 style="
    margin-top: 0.8rem;
    margin-bottom: 0.2rem;
    font-size: 1.05rem;
    text-align: center;
  ">
    {{ member.name }}
  </h3>

  <p style="margin: 0; text-align: center;">
    {{ member.position }}
  </p>

  <p style="margin-top: 0.2rem; font-style: italic; text-align: center;">
    {{ member.duration }}
  </p>

  <p style="
    margin-top: 0.5rem;
    font-size: 0.95rem;
    text-align: center;
  ">
    {{ member.current_affiliation }}
  </p>

</div>

{% endfor %}

</div>

{% include section.html %}
```
