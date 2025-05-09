# Template for Fontys Reports for Obsidian

## 1. Put `pandoc-markdown` somewhere recognizable by your `PATH` like `/usr/local/bin`
## 2. Put [fontys logo](fontys-logo.pdf) and [background](background6.pdf) in your Obsidian Vault, in my case relative path is `Bins/Pandoc-extras` for the logo and `Bins/Pandoc-extras/background` for the background
## 2. Install [Shell commands plugin](obsidian://show-plugin?id=obsidian-shellcommands)
## 3. Add new shell command and put this in `pandoc-markdown {{file_path:relative}}`
## 4. Add a hotkey for it (Optional)

`Go to Obsidian Settings -> Hotkeys -> `

![alt text](obsidian-hotkey.png)

## 5. There are some fields that need to be present in the frontmatter of a file that you want to convert:

```yaml
---
author: Tomasz Olejarczuk
title: Kubernetes Cluster Deployment Proposal
date: 24-02-2025
subject: Kubernetes with Cillium
titlepage: true
titlepage-text-color: "663366"
titlepage-rule-color: "663366"
titlepage-background: 
titlepage-rule-height: 
page-background: Bins/Pandoc-extras/backgrounds/background6.pdf
titlepage-logo: Bins/Pandoc-extras/fontys-logo.pdf
logo-width: 50mm
toc: true
toc-own-page: true
header-left: \hspace{1cm}
header-center: \leftmark
header-right: Page \thepage
footer-left: \thetitle
footer-center: 
footer-right: \theauthor
---
```