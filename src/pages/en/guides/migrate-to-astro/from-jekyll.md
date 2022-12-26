---
title: Migrating from Jekyll
description: Tips for migrating an existing Jekyll project to Astro
layout: ~/layouts/MigrationLayout.astro
stub: true
framework: Jekyll
---

[Jekyll](https://jekyllrb.com) is a static site generator built on Ruby.

## Key Similarities between Jekyll and Astro

Jekyll and Astro share some similarities that will help you migrate your project:

- Both Jekyll and Astro are static-site generators, commonly used to create blogs.

- Jekyll and Astro both allow you to write your content in Markdown and HTML. Astro syntax is a superset of HTML, so creating new pages should feel familiar.

- Both Jekyll and Astro use file-based routing for blog posts. Astro provides a special `src/pages/` directory, and any Astro, Markdown or MDX file contained within that folder creates a page route. Jekyll uses a similar special folder called `_posts/` for your Markdown blog posts, however your site pages can exist elsewhere. Creating new Markdown posts should feel familiar in Astro. Jekyll and Astro both provide some special frontmatter YAML properties for page layout and unpublished draft posts.


## Key Differences between Jekyll and Astro

When you rebuild your Jekyll site in Astro, you will notice some important differences:

- As Jekyll is primarily a blogging platform, several blog features are built-in that you may have to build yourself in Astro, or choose a template theme that includes these features. Jekyll has built in support for tags and categories which you will find in several Astro blog themes, but is not an included feature. Content collections are still an experimental feature in Astro and should be released in v2.

- While Jekyll uses Liquid templates for reusable layout elements, Astro is entirely component-based. Any `.astro` file can be a component, a layout or an entire page, and can import and render any other Astro components. Astro components can also render other UI framework components (e.g. React, Svelte, Vue, Solid) as well as content or meta data from other files in your project, such as Markdown or MDX.


## Switch from Jekyll to Astro

To convert a Jekyll blog to Astro, start with our blog theme starter template, or explore more community blog themes in our [theme showcase](https://astro.build/themes). 

Bring your existing Markdown files as content to [create Markdown pages](/en/guides/markdown-content/), using an Astro component layout instead of a Liquid template. Instead of writing `.html` page files directly, you will write `.astro` files in a language that is a super-set of HTML. Much of your existing HTML page content can transfer into [Astro pages](/en/core-concepts/astro-pages/), and you will additionally be able to [use variables, JSX-like expressions and component imports directly in your HTML templating](/en/core-concepts/astro-components/#jsx-like-expressions).

## Community Resources

- Add your own!