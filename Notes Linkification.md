---
published: True
---

Another opinionated thing: `obsidian-blog` doesn't consider obsidian links that has text around as notes that should be unwrapped into the post. It seems natural (at least for me), that this links should be processed as links.
`obsidian-blog` checks if the notes have `link` attribute in the frontmatter section, and if they do, it replaces this includes as old good html links.

That's really useful on a large vault, when you links to a MoC in a specific note, and you don't want the whole MoC to be populated into your post.
