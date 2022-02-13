---
title: Active Page Context
published: True
links:
  - name: Content Data Implementation
    url: https://github.com/A/obsidian-blog/blob/master/src/dataclasses/content_data.py
---

To get some data from the current page rendered in a handlebars template, you can refere to `self` variable, which has properties listed below:

- `self.content` refers to the rendered html content of the page
- `self.entities` refers to the list of entities parsed from a page and its children. That's useful to render ToCs, etc
- `self.title`
- `self.date`
- `self.slug` is a path after `/` the page is published to
- `self.meta` is a dict contains frontmatter variables of the page

Pages are handlebars templates support a yaml-frontmatter section. Pages stands for anything but posts. 

This is an example of `index.hbs` page renders all posts from the blog:

```handlebars
---
title: Posts
---
<h1>{{ self.title }}</h1>
<ul>
  {{#each posts}}
      <li>
        <span>[{{ this.date }}]: </span>
        <a href="/{{this.slug}}">{{ this.title }}</a>
      </li>
  {{/each}}
</ul>

```
