---
layout: page
title: Blog
permalink: /blog/
---

<div style="text-align: center; margin-bottom: 50px; font-family: sans-serif; color: #828282;">
  <small>CATEGORIES</small><br>
  <a href="#cyber">Cyber Security</a> &nbsp;•&nbsp; 
  <a href="#cs">CS Fundamentals</a> &nbsp;•&nbsp; 
  <a href="#experience">Experience</a> &nbsp;•&nbsp;
  <a href="#wellbeing">Welbeing</a>
</div>

<hr>

<div style="text-align: center; margin: 40px 0;">
  <small>ARTICLES SERIES</small>
</div>

<div id="cyber" style="margin-bottom: 60px;">
  <h2>Cyber Security</h2>
  <p style="font-style: italic; color: #666; font-size: 1.1em;">
    My journey into CTFs, Splunk tools, and understanding exploits from the ground up.
  </p>
  
  {% if site.categories.cyber %}
    <ul class="post-list">
      {% for post in site.categories.cyber %}
        <li>
          <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
          <h3>
            <a class="post-link" href="{{ post.url | relative_url }}">
              {{ post.title | escape }}
            </a>
          </h3>
        </li>
      {% endfor %}
    </ul>
  {% else %}
    <p>No posts yet.</p>
  {% endif %}
</div>

<div id="cs" style="margin-bottom: 60px;">
  <h2>CS Fundamentals</h2>
  <p style="font-style: italic; color: #666; font-size: 1.1em;">
    The magic behind how computers actually work, from OSI models to memory management.
  </p>

  {% if site.categories.cs %}
    <ul class="post-list">
      {% for post in site.categories.cs %}
        <li>
          <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
          <h3>
            <a class="post-link" href="{{ post.url | relative_url }}">
              {{ post.title | escape }}
            </a>
          </h3>
        </li>
      {% endfor %}
    </ul>
  {% endif %}
</div>

<div id="experience" style="margin-bottom: 60px;">
  <h2>Experience</h2>
  <p style="font-style: italic; color: #666; font-size: 1.1em;">
    Real-world projects, internships, and lessons learned in the field.
  </p>

  {% if site.categories.experience %}
    <ul class="post-list">
      {% for post in site.categories.experience %}
        <li>
          <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
          <h3>
            <a class="post-link" href="{{ post.url | relative_url }}">
              {{ post.title | escape }}
            </a>
          </h3>
        </li>
      {% endfor %}
    </ul>
  {% endif %}
</div>

<div id="wellbeing" style="margin-bottom: 60px;">
  <h2>Wellbeing</h2>
  <p style="font-style: italic; color: #666; font-size: 1.1em;">
    Life-lessons taught from elders.
  </p>

  {% if site.categories.wellbeing %}
    <ul class="post-list">
      {% for post in site.categories.wellbeing %}
        <li>
          <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
          <h3>
            <a class="post-link" href="{{ post.url | relative_url }}">
              {{ post.title | escape }}
            </a>
          </h3>
        </li>
      {% endfor %}
    </ul>
  {% endif %}
</div>
