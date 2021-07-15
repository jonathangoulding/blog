---
title: Deploying a vuepress site to GitHub Pages
description: Why use a domain for side projects
---

There are some examples for deploying a Vue app using Github actions that use multiple marketplace actions or a convoluded process.

I found the simplest way is to just use the basic github actions.

Repo: <a href="https://github.com/jonathangoulding/vuepress-docs-example"> Vuepress Doc
Example</a>

```yaml
name: Deploy to Github Pages

on:
  push:
    branches: [main]
  pull_request:
    branches: [main]

  workflow_dispatch:

jobs:
  build-and-deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: Build vuepress and deploy to gh-pages branch
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
        run: |
          # install
          npm ci
          # build
          npm run build
          # navigate into the build output directory
          cd src/.vuepress/dist
          # Git push to gh-pages
          git config --global init.defaultBranch main
          git init 
          git config --local user.email "${GITHUB_ACTOR}"
          git config --local user.name "${GITHUB_ACTOR}"
          git add -A
          git commit -m 'deploy'
          git push -f https://${GITHUB_ACTOR}:${GITHUB_TOKEN}@github.com/${GITHUB_REPOSITORY}.git main:gh-pages
```
