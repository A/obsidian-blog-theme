---
published: True
---

`obsidian-blog` don't publish anything explicitly marked as published in the frontmatter section:

```
---
published: True
---
```

Non-published notes are still being parsed, but ignored during the rendering.

There is also the draft feature. You can annotate your post `draft: True` to make it visible if you start `obsidian-blog` with the `--drafts` flag.
