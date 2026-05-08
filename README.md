# Content guide

This repo now supports two simple content paths:

## Blog posts

Create a file in `_posts/` named like:

```markdown
_posts/2026-05-07-my-post.md
```

Use this shape:

```markdown
---
title: My post title
date: 2026-05-07 09:00:00 +0530
---

Write the post here.
```

## Notes

Create a file in `_notes/` named like:

```markdown
_notes/my-note.md
```

Use this shape:

```markdown
---
title: My note title
---

Write the note here.
```

Notes are published automatically at `/notes/<filename>/` and listed on `/notes/` and the homepage.
