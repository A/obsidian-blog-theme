---
published: True
---

The simplest way to start so far is to copy `.blog` dir from [this repository][obsidian-blog-theme] and tweak css and templates to fit your design.


### Writing

For writing purpose, you can start `obsidian-blog` to watch and serve mode:

```
obsidian-blog --serve --watch
```

This one will start a simple http server on the `localhost:4200` and rebuild your content on any change.


### Building

To build your notes into the static files just run `obsidian-blog` command. Static site will be in the `.build` directory.

[obsidian-blog-theme]: https://github.com/A/obsidian-blog-theme/tree/master/.blog
