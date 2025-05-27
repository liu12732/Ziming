{% raw %}
---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if site.author.googlescholar %}
  <div class="wordwrap">Full list available on <a href="{{site.author.googlescholar}}">Google Scholar</a>.</div>
{% endif %}

{% include base_path %}

<div class="publications-list">
  {% for post in site.publications reversed %}
    {% include archive-single.html %}
  {% endfor %}
</div>
{% endraw %}
