---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

<style>
.pub-scholar-link { margin-bottom: 20px; font-size: 0.95em; }

.pub-card {
  background: #fff;
  border: 1px solid #e0e0e0;
  border-left: 3px solid #093f39;
  border-radius: 4px;
  padding: 7px 12px;
  margin-bottom: 5px;
  transition: box-shadow 0.2s;
}
.pub-card:hover {
  box-shadow: 0 2px 8px rgba(0,0,0,0.08);
}
.pub-title {
  font-size: 0.88em;
  font-weight: 700;
  color: #1a1a1a;
  margin-bottom: 2px;
  line-height: 1.4;
}
.pub-authors {
  font-size: 0.78em;
  color: #555;
  margin-bottom: 3px;
}
.pub-meta {
  display: flex;
  align-items: center;
  gap: 8px;
  flex-wrap: wrap;
}
.pub-venue {
  display: inline-block;
  padding: 1px 7px;
  border-radius: 3px;
  font-size: 0.72em;
  font-weight: 700;
  color: #fff;
  background: #607d8b;
}
.venue-ndss   { background: #1565c0 !important; }
.venue-ccs    { background: #6a1b9a !important; }
.venue-usenix { background: #00695c !important; }
.venue-neurips{ background: #e65100 !important; }
.venue-ieee   { background: #0277bd !important; }
.venue-acm    { background: #558b2f !important; }

.pub-year-badge { font-size: 0.78em; color: #888; }
.pub-award {
  display: inline-flex; align-items: center; gap: 4px;
  background: #fff8e1; border: 1px solid #f9a825;
  color: #e65100; border-radius: 10px;
  font-size: 0.72em; font-weight: 700;
  padding: 2px 9px;
}
</style>

<div class="pub-scholar-link">
{% if site.author.googlescholar %}
  Find full citation list on <a href="{{ site.author.googlescholar }}" target="_blank"><strong>Google Scholar</strong></a>.
{% endif %}
</div>

{% include base_path %}

{% assign sorted_pubs = site.publications | sort: "date" | reverse %}

{% for post in sorted_pubs %}
  {% assign v = post.venue | downcase %}
  {% if v contains "ndss" %}{% assign vc = "venue-ndss" %}
  {% elsif v contains "ccs" %}{% assign vc = "venue-ccs" %}
  {% elsif v contains "usenix" or v contains "security" %}{% assign vc = "venue-usenix" %}
  {% elsif v contains "neurips" or v contains "nips" %}{% assign vc = "venue-neurips" %}
  {% elsif v contains "ieee" or v contains "infocom" or v contains "dsn" or v contains "tdsc" or v contains "ton" or v contains "tmc" %}{% assign vc = "venue-ieee" %}
  {% elsif v contains "acm" %}{% assign vc = "venue-acm" %}
  {% else %}{% assign vc = "" %}
  {% endif %}

<div class="pub-card">
  <div class="pub-title"><a href="{% if post.paperurl %}{{ post.paperurl }}{% else %}{{ post.url }}{% endif %}" {% if post.paperurl %}target="_blank"{% endif %} style="color:inherit;text-decoration:none;">{{ post.title }}</a></div>
  <div class="pub-authors">{{ post.author }}</div>
  <div class="pub-meta">
    <span class="pub-venue {{ vc }}">{{ post.venue }}</span>
    <span class="pub-year-badge">{{ post.date | date: "%Y" }}</span>
    {% if post.award %}<span class="pub-award">🏆 {{ post.award }}</span>{% endif %}
    <a href="https://scholar.google.com/scholar?q={{ post.title | url_encode }}" target="_blank" style="font-size:0.78em;color:#2a7ae2;text-decoration:none;">Cite ↗</a>
  </div>
</div>
{% endfor %}
