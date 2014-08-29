# A Standard Jekyll Template

This is  a standard template for [Jekyll](http://jekyllrb.com), everything you might expect from a starter site.

[Check it out »](http://blacktm.github.io/standard-jekyll-template)

Tweet feedback to [@blacktm](https://twitter.com/blacktm).

## Features

Some of the fancy, out-of-the-box features of this template:

- Minimally responsive design
- Easy to configure without too much layout hacking
- Includes an "edit page" link to encourage OSS love
- Table of contents for documentation-like content
- Lots Jekyll best practices on display
- Easily customizable, whether style or structure
- Uses [`normalize.css`](http://necolas.github.io/normalize.css/) for CSS resets
- Uses [Colors](http://clrs.cc) for colors

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

### Page and Post Options:

This goes in the YAML front matter:

```yaml
---
edit_page: boolean  # Show/hide the edit page link
                    # Overrides _config.yml

toc: string  # Specify the table of contents to use
             # This is the file name in the _data/ directory
---
```

## Using the Table of Contents

To use the built-in table of contents, set the layout to `toc` in the YAML front matter:

```yaml
---
layout: toc
---
```

Then add headings, pages, and links to `_data/toc.yml` or to a custom `.yml` file if using multiple TOCs. Use the format here:

```yaml
- heading:
    text: string - heading text
    link: string - heading link
  pages:
  - text: string - page text
    link: string - page link
```

See [`toc.yml`](_data/toc.yml) for a detailed example.

## Editing the Template

To help keep the template easy to upgrade and maintain, try to limit editing to these directories and files:

```no-highlight
_data/
_includes/  -- only edit the two files below
  _fonts.html
  _footer.html
_posts/
_sass/  -- don't edit anything named "template"
blog/
css/    -- `main.scss` contains the final compiled styles
docs/   -- just an example directory, can remove
img/
js/     -- don't edit the `template/` directory inside
```

## Why Make a Template?

I use Jekyll and GitHub pages for everything, [and I mean everything](https://github.com/department-of-veterans-affairs/gi-bill-comparison-tool). For new projects, I wanted the ability to spin up a site quickly, where minimal layout hacking was required and all the content placeholders were there. It needed to be comprehensive enough to meet the expectations of a mobile-first, responsive site yet simple to configure, customize, and extend. It also had to be easy to keep up to date, since I often have to maintain a bunch of OSS sites and such. If anything, it's a great template to learn from, given all the incredible features, power, and extensibility of Jekyll. :heart:
