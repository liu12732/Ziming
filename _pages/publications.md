---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% assign sorted_pubs = site.publications | sort: 'date' | reverse %}

<ol class="publication-list reversed">
  {% for pub in sorted_pubs %}
    {% assign index = sorted_pubs.size | minus: forloop.index0 %}
    <li class="publication-item">
      <span class="pub-meta">
        {% if pub.collaborators %}
          (with {{ pub.collaborators }})
        {% endif %}
      </span>
      <a href="{{ pub.link }}" class="pub-title">{{ pub.title }}</a>
      {% if pub.journal %}
        <span class="pub-journal">, {{ pub.journal }}</span>
      {% else %}
        <span class="pub-preprint"> (Preprint)</span>
      {% endif %}
    </li>
  {% endfor %}
</ol>
