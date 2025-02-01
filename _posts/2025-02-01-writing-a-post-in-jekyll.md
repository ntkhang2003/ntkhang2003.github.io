---
layout: post
title: Writing a Post in Jekyll
description: This tutorial will help you write a blog/post with Jekyll.
date: 2025-02-01 23:59 +0700
categories: [Jekyll]
tags: [getting started]
author: khang
---

## Path
All posts of your site must be placed in `_post` directory. 

## Naming
Create a new file with format `YYYY-MM-DD-TITLE.EXTENSION` where `YEAR` is a four-digit number, `MONTH` and `DAY` are both two-digit numbers, e.g `2025-02-01-get-started-with-jekyll.md`. Note that the `EXTENSION` must be one of [md/markdown](https://en.wikipedia.org/wiki/Markdown) or html. To save time manually creating files, you should use [jekyll-compose](https://github.com/jekyll/jekyll-compose).

## Front Matter 

All blog post files must begin with [front matter](https://jekyllrb.com/docs/front-matter/) to set a layout or other meta data as below:

```yaml
---
layout: LAYOUT
title: TITLE
date: YYYY-MM-DD HH:MM:SS +/-TTTT
categories: [TOP_CATEGORIE, SUB_CATEGORIE]
tags: [tag]     # TAG names should always be lowercase
author: <author_name>
published: true
---
```

Or using [jekyll-compose](https://github.com/jekyll/jekyll-compose) by running `bundle exec jekyll post "TITLE"`.

### Layout
If set, this specifies the layout file to use. Use the layout file name without the file extension. Layout files must be placed in the `_layouts` directory.

### Date
A date is specified in the format `YYYY-MM-DD HH:MM:SS +/-TTTT`; hours, minutes, seconds, and timezone offset are optional.

### Categories
Categories can be specified as a [YAML list](https://en.wikipedia.org/wiki/YAML#Basic_components) or a space-separated string.

### Tags
Similar to categories, one or multiple tags can be added to a post

### Author
Use this to provide author's name.

### Published
Set to false if you don’t want a specific post to show up when the site is generated.

### Custom Variables
You can also set your own front matter variables you can access in [Liquid](https://jekyllrb.com/docs/liquid/) (with layout from `_layout` directory). For instance, if you set a variable called `description` to briefly describe your post, you can use that in your page:

```yaml
---
description: Short summary of the post.
---

<h2>{{ page.description }}</h2>
```

## Writing Blog/Post
After setting Front Matter, you just need to use markdown to write your content, and I recommend the beginners to use [stackedit](https://stackedit.io/ "markdown editor tool") or [editor md](https://pandao.github.io/editor.md/en.html).

Then run `bundle exec jekyll s` to check the blog on the interface before `committing` to GitHub repository.

## Conclusion
I have shown you the general way to write basic blog, you should consider the documents of your theme for more customized content. Please waiting for LLMs-related content, I will be soon!
