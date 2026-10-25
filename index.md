---
layout: page
title: Study Hub
---

<style>
.study-hero {
  padding: 2.4rem;
  margin: .5rem 0 2rem;
  color: #f8fafc;
  background: linear-gradient(135deg, #172554, #1d4ed8 58%, #0891b2);
  border-radius: 1.25rem;
  box-shadow: 0 18px 45px rgba(15, 23, 42, .18);
}
.study-hero h1 { margin: 0 0 .6rem; font-size: clamp(2rem, 7vw, 3.6rem); }
.study-hero p { max-width: 42rem; margin: 0; color: #dbeafe; font-size: 1.08rem; }
.study-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(220px, 1fr)); gap: 1rem; margin: 0 0 2rem; }
.study-card {
  display: block;
  padding: 1.25rem;
  color: #0f172a !important;
  background: #fff;
  border: 1px solid #dbe3ef;
  border-radius: 1rem;
  box-shadow: 0 8px 24px rgba(15, 23, 42, .08);
  text-decoration: none !important;
  transition: transform .16s ease, box-shadow .16s ease, border-color .16s ease;
}
.study-card:hover { transform: translateY(-3px); border-color: #60a5fa; box-shadow: 0 14px 32px rgba(15, 23, 42, .14); }
.study-card strong { display: block; margin-bottom: .35rem; color: #1d4ed8; font-size: 1.1rem; }
.study-card span { color: #475569; line-height: 1.5; }
.study-section { margin-top: 2rem; }
.repo-link { display: inline-flex; align-items: center; gap: .45rem; padding: .7rem 1rem; border: 1px solid #cbd5e1; border-radius: 999px; text-decoration: none !important; font-weight: 650; }
</style>

<section class="study-hero">
  <h1>Study Hub</h1>
  <p>Practice exams, physics tools, programming review, and course notes in one place.</p>
</section>

<div class="study-grid">
  <a class="study-card" href="/emf.html">
    <strong>EMF midterm practice</strong>
    <span>125 exam and WebAssign questions with answer reveals and saved progress.</span>
  </a>
  <a class="study-card" href="/dsa_exam_practice.html">
    <strong>CS 1134 DSA exam practice</strong>
    <span>Review data structures and algorithms with focused practice questions.</span>
  </a>
  <a class="study-card" href="/oops.html">
    <strong>OOP C++ practice</strong>
    <span>Practice object-oriented programming concepts and exam problems.</span>
  </a>
  <a class="study-card" href="/mobile-physics.html">
    <strong>Mobile physics practice</strong>
    <span>A compact physics practice page designed for smaller screens.</span>
  </a>
  <a class="study-card" href="/notes/">
    <strong>Course notes</strong>
    <span>Browse the published collection of study notes.</span>
  </a>
</div>

<a class="repo-link" href="https://github.com/pragundamani/pragundamani.github.io">View this site on GitHub →</a>

<section class="study-section">
  <h2>Recent posts</h2>
  {% assign posts = site.posts | sort: 'date' | reverse %}
  {% if posts.size > 0 %}
  <ul>
  {% for post in posts limit: 10 %}
    <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
  {% endfor %}
  </ul>
  {% else %}
  <p>No posts yet.</p>
  {% endif %}
</section>

<section class="study-section">
  <h2>Notes</h2>
  {% assign notes = site.notes | sort: 'title' %}
  {% if notes.size > 0 %}
  <ul>
  {% for note in notes limit: 10 %}
    <li><a href="{{ note.url | relative_url }}">{{ note.title | default: note.basename }}</a></li>
  {% endfor %}
  </ul>
  {% else %}
  <p>No notes yet.</p>
  {% endif %}
</section>
