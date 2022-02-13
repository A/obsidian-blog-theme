---
published: True
---

`obsidian-blog` supports `.env`, and it seems a pretty good place to define your `blog_title` and other specific settings. A list of variables is [here][obsidian-blog-config].

Another way is to use cli flags. Take a look on `obsidian-blog --help` for a list of supported options:

```
notes ❯ obsidian-blog --help
obsidian-blog

Static site generator for obsidian.md notes.

Usage:
  obsidian-blog [-d] [-w] [-s] [--port <number>] [--title <string>] [--posts_dir <directory>] [--pages_dir <directory>]

Options:
  -h --help                     Show this screen.
  -w --watch                    Enable watcher
  -s --serve                    Enable web-server
  -p --port=<number>            Web-server port [default: 4200]
  -d --drafts                   Render draft pages and posts

  --title=<string>              Blog title [default: My Blog]

  --version             Show version.
```

[obsidian-blog-config]: https://github.com/A/obsidian-blog/blob/master/src/dataclasses/config_data.py#L7
