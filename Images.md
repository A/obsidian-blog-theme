---
title: Images
published: True
---

Images are processed in 2 steps:

### Parsing

All images are parsed into `asset_entity` objects contains their placeholders, alts, and urls.

### Building

During the build image files are copied under `.build` dir, and urls are updated accordingly. Then images are rendered into HTML.

To point to a specific image, use `config.public_dir` prefix in a handlebars template.
