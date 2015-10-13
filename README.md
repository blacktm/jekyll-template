# A Standard Jekyll Template

This is  a standard template for [Jekyll](http://jekyllrb.com), everything you might expect from a starter site.

[Check it out »](http://blacktm.github.io/standard-jekyll-template)

Serve locally using `jekyll serve --watch --baseurl ""` or running `bash serve.sh`.

Tweet feedback to [@blacktm](https://twitter.com/blacktm).

## Features

Some of the fancy, out-of-the-box features of this template:

- Basic responsive design, mobile menus
- Easy to configure with YAML site config and front matter
- An "edit page" link to GitHub to encourage OSS love
- Optional contents list for navagating long pages
- Gets out of the way to easily customize style and structure
- Uses [Normalize.css](http://necolas.github.io/normalize.css/) for CSS resets
- Uses [Colors](http://clrs.cc) for colors
- Lots Jekyll best practices on display

## Sites Using this Template

- [blacktm.com](http://www.blacktm.com)
- [ruby2d.com](http://www.ruby2d.com)
- [bluebuttonjs.com](http://www.bluebuttonjs.com)

## Configuration Options

Options can either be set in [`_config.yml`](_config.yml) or in a page's YAML front matter. If options are shared between both, the front matter takes higher precedence. Below are the template-specific config options.

### `_config.yml` Options:

```yaml
# Site config - required by template
title:       string  # The site's title
description: string  # The site's description
baseurl:     string  # Serve the site from the given URL
url:         string  # The site's URL

# Header config
header:
  logo_text: string  # Text to the right of the logo
  logo_img:  string  # Path of the logo image
  nav:  # Array of text/links for the header
    - text:  string  # Text of the link
      link:  string  # Path of the link

# Edit Page config
edit_page:
  # enabled: true   # Enabled by default for pages and posts
  text:     string  # The text to display for the edit page link
  github:   # Object containing the pertinent GitHub info to construct the link
    author: string
    repo:   string
    branch: string
```

### Page Options:

This goes in the YAML front matter:

```yaml
---
title: string       # Title of the page
subtitle: string    # Subtitle of the page

breadcrumbs:
  - text: string    # Text of the link
    link: string    # Link href

contents:
  - text: string    # Text of the link
    link: string    # Link href

edit_page: boolean  # Show/hide the edit page link
                    # Overrides _config.yml

header: boolean     # Set to false to hide the header on the page
footer: boolean     # Set to false to hide the footer on the page

css: string         # Sets a CSS class for the current page
---
```

### Post Options:

```yaml
---
edit_page: boolean  # Show/hide the edit page link
                    # Overrides _config.yml
---
```

To change the posts path (e.g. "/blog" to "/news"), edit the following:

1. In `_config.yml` where `<path>` is the desired URL path:
    
    ```yaml
    # Posts
    posts_path: /<path>
    permalink: "/<path>/:year/:month/:day/:title"

    # Pagination
    paginate_path: "/<path>/page:num"
    ```

2. Rename `/blog` directory to `<path>`.

3. Change permalink in `/<path>/categories.html`:
    
    ```yaml
    permalink: /<path>/categories/
    ```

## Maintaining the Template

When using this template for your own site, try not to edit any files or directories named `template` for ease of updating and maintaining.

## Why Make a Template?

I use Jekyll and GitHub pages for everything, [and I mean everything](https://github.com/department-of-veterans-affairs/gi-bill-comparison-tool). For new projects, I wanted the ability to spin up a site quickly, where minimal layout hacking was required and all the content placeholders were there. It needed to be comprehensive enough to meet the expectations of a mobile-first, responsive site yet simple to configure, customize, and extend. It also had to be easy to keep up to date, since I often have to maintain a bunch of OSS sites and such. If anything, it's a great template to learn from, given all the incredible features, power, and extensibility of Jekyll. :heart:
