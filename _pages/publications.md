---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if site.author.googlescholar %}
  <p>Complete list on <a href="{{ site.author.googlescholar }}">Google Scholar</a></p>
{% endif %}

{% include base_path %}

<div class="publications-container">
  {% for post in site.publications reversed %}
    {% include archive-single.html %}
  {% endfor %}
</div>
