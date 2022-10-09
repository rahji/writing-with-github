# Publishing Using GitHub Pages

Publishing a repository of Markdown files as a website can be as simple as going to the repository's Settings on the GitHub website and enabling GitHub Pages. GitHub Pages can host your repo as a website and synchronize the two whenever you push to the repository. This process can get more involved if you want to heavily customize the website or preview the generated website locally before pushing to GitHub, but the process described here will get your website published with minimal effort.

1. Click the Settings link on your repo's GitHub page
2. Choose Pages from the menu on the left
3. Select `Deploy from a branch` as the Source
4. Choose your main branch and the `/root` folder
5. Click Save and refresh this page until you see a message saying that your site is live

## Customizing the Website

```yaml
remote_theme: pages-themes/minimal@v0.2.0
title: Writing with GitHub
description: A proposed system for writing using Git, GitHub, VS Code, and Markdown
plugins:
- jekyll-remote-theme
```

Several Jekyll themes are supported by GitHub Pages. The list can be found at <https://pages.github.com/themes/>. 

## More Information

* [GitHub Pages Documentation](https://docs.github.com/en/pages)
