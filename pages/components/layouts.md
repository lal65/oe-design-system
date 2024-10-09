---
title: 'Components - Layouts'
meta:
  robots: 'noindex, nofollow'
  description: 'Layouts are flexible, special purpose containers designed specifically for containing components. Examples of layouts include multi-column and grids.'
page_subtitle_before: 'Components'
page_title: 'Layouts'
page_subtitle_after: 'Penn State World Campus'
menu_link_title: 'Layouts'
sort_order: 5
---

{% apply markdown_to_html %}
  Layouts are flexible, special purpose containers designed specifically for
  containing components. Examples of layouts include multi-column and grids.
{% endapply %}

{% include 'partials/grid-submenu.twig' with {
  heading: {
    content: 'Explore the various layouts',
    level: 2,
  },
  path: 'components/layouts',
} only %}
