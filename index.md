---
layout: page
title: Home
---

# Home

## Add content fast

- New blog post: create `_posts/YYYY-MM-DD-title.md`
- New note: create `_notes/title.md`
- New standalone tool/page: add the file in the repo root, then link it below

## Pages

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
