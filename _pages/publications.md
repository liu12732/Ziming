---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% assign pub_count = site.publications | size %}
{% assign reversed_pubs = site.publications | reverse %}

{% if site.author.googlescholar %}
  <p>Complete list on <a href="{{ site.author.googlescholar }}">Google Scholar</a></p>
{% endif %}

<div class="publications-list">
  {% for post in reversed_pubs %}
    <div class="pub-item">
      <span class="pub-number">{{ pub_count | minus: forloop.index0 }}.</span>
      <div class="pub-content">
        <a href="{{ post.link }}" class="pub-title">
          {{ post.authors }} {{ post.title }}
        </a>
        {% if post.journal %}
          <span class="pub-journal">, {{ post.journal }}</span>
        {% else %}
          <span class="pub-preprint"> (Preprint)</span>
        {% endif %}
      </div>
    </div>
  {% endfor %}
</div>
