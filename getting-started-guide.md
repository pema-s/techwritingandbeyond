---
title: "How to create a Getting Started guide for API Docs"
keywords: "api documentation, api, documentation, dev docs, developer, documentation, technical, writers" 
tags: [getting_started]
sidebar: mydoc_sidebar
permalink: getting-started-guide.html
folder: techwritingandbeyond
---

### 1. Download the theme

First, download or clone the theme from the [Github repo](https://github.com/tomjoht/documentation-theme-jekyll). Most likely you won't be pulling in updates once you start customizing the theme, so downloading the theme (instead of cloning it) probably makes the most sense. In Github, click the **Clone or download** button, and then click **Download ZIP**.

### 2. Install Jekyll

If you've never installed or run a Jekyll site locally on your computer, follow these instructions to install Jekyll:

* [Install Jekyll on Mac][mydoc_install_jekyll_on_mac]
* [Install Jekyll on Windows][mydoc_install_jekyll_on_windows]

### 3. Install Bundler

In case you haven't installed Bundler, install it:

```
gem install bundler
```

You'll want [Bundler](http://bundler.io/) to make sure all the Ruby gems needed work well with your project. Bundler sorts out dependencies and installs missing gems or matches up gems with the right versions based on gem dependencies.

### 4. Option 1: Build the Theme (*without* the github-pages gem) {#option1}

Use this option if you're not planning to publish your Jekyll site using [Github Pages](https://pages.github.com/).

Bundler's Gemfile specifies how project dependencies are managed. Although this project includes a Gemfile, this theme doesn't have any dependencies beyond core Jekyll. The Gemfile is used to list gems needed for publishing on Github Pages. **If you're not planning to have Github Pages build your Jekyll project, delete these two files from the theme's root directory:**

* Gemfile
* Gemfile.lock
