---
title: Using the Theme
date: 2021-12-02
category: Blog
---
# Using minimal mistakes
I'm just taking some notes on features I might want to keep in mind when writting posts. Mostly reading through the theme documentation.

## Header images
Header images for individual posts. The documentation recomends a width of 1280px.
Frontmatter:
```yaml
---
header:
  image: /assets/images/image-filename.jpg
  image_description: "A description of the image"
  caption: "Photo credit: [**Unsplash**](https://unsplash.com)"
---
```

There's more about header overlay - writting text on top of image. I don't see myself bothering with that for a while, this note might serve as a reminder.

## Navigation
Navigational links, like the lone "Quick-Start Guide" that's currently available, are read from: `_data/navigation.yml`.
Example from the docs:
```yaml
main:
  - title: "Quick-Start Guide"
    url: /docs/quick-start-guide/
  - title: "Posts"
    url: /year-archive/
  - title: "Categories"
    url: /categories/
  - title: "Tags"
    url: /tags/
  - title: "Pages"
    url: /page-archive/
  - title: "Collections"
    url: /collection-archive/
  - title: "External Link"
    url: https://google.com
```
With this I can add my main page, dnd, foundry and other links as I see fit.

## Collections, categories, tags?
I'd like to have a categories page where the most recent category being at the top. From messing around a bit that seems like a no go.
Next up is collections or categories I guess. I'd like to seperate 3d modeling shenannigans from 3d printing, linux and whatnot.