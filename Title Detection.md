---
published: True
---

`obsidian-blog` has a title-detection mechanism:

1. If note was included with inline title like `[[this | one]]`, the `one` will be a title
2. If note has a `title` attribute in the frontmatter section, it will be used.
3. Otherwise a filename will be used as a title.

### Filename Title Delimeters

If note has no other title then a filename, and filename contains the delimeter (` - `), the rightest section will be used as a title. This helps if you name your notes with a category prefix, like `Prometheus - PromQL Selectors.md` becomes `PromQL Selectors`. It's a bit opinionated, but this convention saves time.
