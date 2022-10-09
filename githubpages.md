# Publishing Using GitHub Pages

Publishing a repository of Markdown files as a website can be as simple as going to the repository's Settings on the GitHub website and enabling GitHub Pages. GitHub Pages hosts your repo as a website and synchronizes the two whenever you push to the repository. This process can get more involved if you want to heavily customize the website or preview the generated website locally before pushing to GitHub, but the process described here will get a website published with minimal effort.

1. Click the Settings link on your repo's GitHub page
2. Choose Pages from the menu on the left
3. Select `Deploy from a branch` as the Source
4. Choose your main branch and the `/root` folder
5. Click Save and refresh this page until you see a message saying that your site is live. It usually takes a minute or two.

## Customizing the Website

### Applying a Theme

The easiest way to change the look and feel of the published website is to add a theme. The list of supported themes can be found at <https://pages.github.com/themes/>. To apply a theme, create a file in the root of your repo called `_config.yml`. Edit the file and use the contents below as a template for your site configuration.

```yaml
remote_theme: pages-themes/minimal@v0.2.0
title: YOUR SITE NAME
description: YOUR SITE DESCRIPTION
plugins:
- jekyll-remote-theme
```

The above example uses the "minimal" theme. To apply a different theme, adjust the `remote theme` line according to the instructions found in the preferred theme's GitHub repo.

### Changing a Page's Title and URL

Each Markdown page can begin with a [front matter block](https://jekyllrb.com/docs/front-matter/) that contains metadata about the page. An example of information that might be contained in this section includes a title for the page (which is otherwise drawn from the top-level heading of the Markdown text). Another common use for this section is specifying a "permalink" for the page. This will become the URL for the web page. By default, the URL is derived from the Markdown filename. In the example below, both a title and permalink are specified. Again, this code would appear at the top of a Markdown document.

```yaml
---
title: My Specific Page title
permalink: /specific
---
```

### Designating Home and Error Pages

To designate a Markdown document as the home page for your site, set the `permalink` value to `/` in that page's front matter section.

When a reader attempts to browse to a non-existing web page, they will receive a 404 error. To make a custom Markdown page that will be presented when this occurs, create a Markdown document called `404.md` and include the following front matter at the top.

```yaml
---
permalink: /404.html
---
```

## More Information

* [GitHub Pages Documentation](https://docs.github.com/en/pages)
* [Documentation for Jekyll](https://jekyllrb.com/docs/github-pages/), the software that powers GitHub Pages behind the scenes
