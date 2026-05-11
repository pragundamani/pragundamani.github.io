---
layout: page
title: Home
---

# Home

## Pages
- [OOP c++ practice](/oops.html)
- [Mobile physics practice page](/mobile-physics.html)
- [Notes](/notes/)

## Recent posts

{% assign posts = site.posts | sort: 'date' | reverse %}
{% if posts.size > 0 %}
{% for post in posts limit: 10 %}
- [{{ post.title }}]({{ post.url | relative_url }})
{% endfor %}
{% else %}
No posts yet.
{% endif %}

## Notes

{% assign notes = site.notes | sort: 'title' %}
{% if notes.size > 0 %}
{% for note in notes limit: 10 %}
- [{{ note.title | default: note.basename }}]({{ note.url | relative_url }})
{% endfor %}
{% else %}
No notes yet.
{% endif %}
