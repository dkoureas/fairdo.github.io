---
title: Home
layout: base
permalink: /
---

<section class="usa-section home-hero bg-tan" markdown="0">
  <div class="usa-grid">
    <h1 class="mb4">{{ site.description }}</h1>
    <a class="usa-button usa-button-big usa-button-primary m0 no-print" href="{{ '/about/' | relative_url }}">Learn more</a>
  </div>
</section>

<section class="usa-section home-grid" markdown="0">
  <div class="usa-grid md-flex">
    <a href="{{ '/wg/' | relative_url }}" class="usa-width-one-half p3 lg-p4 clearfix">
      <i class="fas fa-user-cog" aria-hidden="true"></i>
      <div class="overflow-hidden">
        <h3 class="arrow">Working Groups</h3>
        <p class="my0">Learn about the various working groups.</p>
      </div>
    </a>
    <a href="{{ '/publications/' | relative_url }}" class="usa-width-one-half p3 lg-p4 clearfix">
      <i class="fas fa-book" aria-hidden="true"></i>
      <div class="overflow-hidden">
        <h3 class="arrow">Publications</h3>
        <p class="my0">Publications related to the FAIR Digital Object concept.</p>
      </div>
    </a>
</div>
<div class="usa-grid md-flex">
    <a href="{{ '/examples/' | relative_url }}" class="usa-width-one-half p3 lg-p4 clearfix">
      <i class="fas fa-atom" aria-hidden="true"></i>
      <div class="overflow-hidden">
        <h3 class="arrow">Examples</h3>
        <p class="my0">See FAIR Digital Objects in action.</p>
      </div>
    </a>
    <a href="{{ '/about/' | relative_url }}" class="usa-width-one-half p3 lg-p4 clearfix">
      <i class="fas fa-info-circle" aria-hidden="true"></i>
      <div class="overflow-hidden">
        <h3 class="arrow">About</h3>
        <p class="my0">More about FAIR Digital Objects.</p>
      </div>
    </a>
  </div>
</section>

<section class="usa-section bg-tan home-events" markdown="0">
  <div class="usa-grid">
    <h2 class="mt0 mb3">Upcoming events and News</h2>
    {% assign events = site.data.events | sort: 'date' %}
    {% assign events_sorted = events | reverse %}
    {% for event in events_sorted %}
      <p class="m0 h5 caps sans-serif">{{ event.date | date: "%B %e, %Y" }}</p>
      <h4 class="m0 h3">{% if event.link %}<a href="{{ event.link }}" class="text-decoration-none">{% endif %}{{ event.title }}{% if event.link %}</a>{% endif %}</h4>
      {% if event.description %}{{ event.description | markdownify }}{% endif %}
    {% endfor %}
  </div>
</section>

<section class="usa-section" markdown="0">
  <div class="usa-grid">
    <h2 class="mt0">About</h2>
    <div class="usa-width-two-thirds md-pr5">
    <p class="usa-font-lead">

The FAIR Digital Object is a Digital Object (DO) (DO as defined by <a href="https://en.wikipedia.org/wiki/Bob_Kahn">Robert Kahn</a> in the early 1990s) that brings together the idea of interoperable digital objects and <a href="https://doi.org/10.1038/sdata.2016.18">FAIR principles</a> together. FAIR Digital Objects can represent data, software, protocols or other research resources. They are accompanied by persistent identifiers (PID) and metadata rich enough to enable them to be reliably found, used and cited (<a href="https://doi.org/10.23728/b2share.2317b12321764f669c92ebbcf7518164">FAIR Implementation Report, Wittenburg & Strawn 2019</a>).
</p>
    </div>
    <div class="usa-width-one-third">
      <h3>Subscribe to our mailing list</h3>
        <p>Learn about upcoming events related to FAIR Digital Objects.</p>
        <a class="usa-button usa-button-primary block m0 nowrap" href="https://fairdo.org/">Subscribe</a>
    </div>
  </div>
</section>
