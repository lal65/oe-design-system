---
title: 'Components - Pages'
meta:
  robots: 'noindex, nofollow'
  description: 'Pages are the highest order of component and are the most opinionated in nature.'
page_subtitle_before: 'Components'
page_title: 'Pages'
page_subtitle_after: 'Penn State World Campus'
menu_link_title: 'Pages'
sort_order: 7
---

{% apply markdown_to_html %}
  Pages are the highest order of component and are the most opinionated in
  nature.

{% endapply %}

{% include 'partials/grid-submenu.twig' with {
  heading: {
    content: 'Explore the various pages',
    level: 2,
  },
  path: 'components/pages',
} only %}
