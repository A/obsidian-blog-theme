---
published: True
---

Parser starts at 2 main directories: `Pages` and `Posts`. It recursively processes all embedded notes if they are placed on the new line and don't have any text around. Parser also supports cycles detection, and shouldn't fail in this case.

Parser recursively collects all entities (such as images, notes, links, etc) from your posts and pages and build a flat list of them.
