---
title: Global Context
published: True
---

`global_context` is always accessible in all handlebars templates (layouts, pages)  and includes few variables:

```
{
  "config": Config
  "self": Page, # refers to the active page
  "layouts": dict[str, Layout],
  "posts": list[Page], # list of posts
  "pages": list[Page], # list of pages
})
```
