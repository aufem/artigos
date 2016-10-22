---
title: Blog
body_classes: 'header-image fullwidth'
blog_url: blog
taxonomy:
    blog:
        - blog
blog_url: blog
sitemap:
    changefreq: daily
    priority: 1.03
content:
    items: '@self.children'
    order:
        by: date
        dir: asc
    limit: 0
    pagination: true
    limit: 1
feed:
    description: 'Blog | Autonomia Feminista'
    limit: 10
---