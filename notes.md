---
layout: page
title: Notes
permalink: /notes/
---

# Notes

Add a new note by creating a Markdown file in `_notes/` with front matter like:

```markdown
---
title: My new note
---

Write here.
```

{% assign notes = site.notes | sort: 'title' %}
{% if notes.size > 0 %}
{% for note in notes %}
- [{{ note.title | default: note.basename }}]({{ note.url | relative_url }})
{% endfor %}
{% else %}
No notes yet.
{% endif %}
