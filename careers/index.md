---
layout: page
---

<div style="display: flex; flex-direction: column; align-items: center; gap: 1rem; margin-top: 2rem;">

{% assign careers = site.pages | where_exp: "c", "c.path contains 'careers/'" | sort: "title" %}
{% for career in careers %}
  {% unless career.name == "index.md" %}
  <a href="{{ career.url | relative_url }}" style="
    display: block;
    width: 300px;
    padding: 1rem 2rem;
    text-align: center;
    border: 2px solid #ccc;
    border-radius: 8px;
    font-size: 1.1rem;
    text-decoration: none;
  ">{{ career.card_title }}</a>
  {% endunless %}
{% endfor %}

</div>
