---
published: True
links:
  - name: GitHub Actions Documentation
    url: https://docs.github.com/en/actions
  - name: Managing a custom domain for your GitHub Pages site
    url: https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site
---

It's quite easy to build and deploy a static site to your own domain:

```
name: Deploy GitHub Pages

on:
  push:
    branches:
      - "master"

env:
  PYTHON_VERSION: 3.10.2

jobs:
  build-and-deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - uses: actions/setup-python@v2
        with:
          python-version: ${{ env.PYTHON_VERSION }}
      - name: install obsidian-blog
        run: pip install obsidian-blog

      - name: build static site
        run: obsidian-blog

      - name: Add gh-pages CNAME
        run: echo ${{ secrets.DOMAIN }} > .build/CNAME

      - uses: JamesIves/github-pages-deploy-action@4.1.4
        with:
          branch: gh-pages
          folder: .build
```
