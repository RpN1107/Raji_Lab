---
title: Contact
nav:
  order: 5
  tooltip: Email, address, and location
---

# {% include icon.html icon="fa-regular fa-envelope" %}Contact

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor
incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis
nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.

{%
  include button.html
  type="email"
  text="rajeswari@labs.iisertirupati.ac.in"
  link="rajeswari@labs.iisertirupati.ac.in"
%}
{%
  include button.html
  type="phone"
  text="(555) 867-5309"
  link="+1-555-867-5309"
%}
{%
  include button.html
  type="address"
  tooltip="Our location on Google Maps for easy navigation"
  link="https://maps.app.goo.gl/wX2HCu5TEv14qqH7A"
%}

{% include section.html %}

{% endcapture %}

{% include cols.html col1=col1 col2=col2 %}

{% include cols.html col1=col1 col2=col2 col3=col3 %}
