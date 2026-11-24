---
layout: page
title: Home
---

<section class="hero">
  <p class="eyebrow">PERSONAL SITE / WORK IN PROGRESS</p>
  <h1>Hey, welcome to <span>HackZach</span>.</h1>
  <p class="hero-copy">A home for ideas in progress, interesting rabbit holes, and notes worth keeping.</p>
  <a class="button-link" href="{{ '/thoughts/' | relative_url }}">Read the blog <span aria-hidden="true">→</span></a>
</section>

<div class="home-grid">
  <section class="content-card" id="intro">
    <p class="eyebrow">01 / INTRO</p>
    <h2>A little about me</h2>
    <p class="edit-hint">Your intro goes here. Add a few lines about yourself, what you're into, or what you're working on.</p>
  </section>

  <section class="content-card" id="links">
    <p class="eyebrow">02 / ELSEWHERE</p>
    <h2>Find me around</h2>
    <p class="edit-hint">Add links to your projects, profiles, or favorite corners of the web here.</p>
  </section>
</div>

<section class="latest-section">
  <div class="section-heading">
    <div>
      <p class="eyebrow">03 / RECENT TRANSMISSIONS</p>
      <h2>Fresh thoughts</h2>
    </div>
    <a class="text-link" href="{{ '/thoughts/' | relative_url }}">All posts <span aria-hidden="true">↗</span></a>
  </div>
  <div class="post-grid">
    {% for post in site.posts limit:2 %}
      <article class="post-card">
        <p class="post-meta">{{ post.date | date: "%b %-d, %Y" }} <span>·</span> SAMPLE</p>
        <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
        <p>{{ post.excerpt | strip_html | truncate: 140 }}</p>
      </article>
    {% endfor %}
  </div>
</section>
