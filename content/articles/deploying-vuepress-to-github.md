---
title: Deploying a vuepress site to GitHub Pages
description: Why use a domain for side projects

---

# Deploying a vuepress site to GitHub Pages

I wanted to explore Github actions and understand how to deploy a website that has a
build step.
I had read a few tutorial that did some complicated things. Some even required
multiple 'marketplace' actions.
This seemed too complicated. So i tried to make it work with just a GitHub action
and config for my <a href="https://github.com/jonathangoulding/vuepress-docs-example"> Vuepress Doc
Example</a> repo.
```yaml
name: Deploy to Github Pages

on:
  push:
    branches: [ main ]
  pull_request:
    branches: [ main ]
    
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
