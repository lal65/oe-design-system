---
title: 'Components - Blocks'
meta:
  robots: 'noindex, nofollow'
  description: 'Blocks are complete, opinionated design concepts offer turn-key functionality and are expected to be added directly to layouts, regions, and pages. Some examples include page titles, and special use menus.'
page_subtitle_before: 'Components'
page_title: 'Blocks'
page_subtitle_after: 'Penn State World Campus'
menu_link_title: 'Blocks'
sort_order: 4
---

{% apply markdown_to_html %}
  Blocks are complete, opinionated design concepts offer turn-key functionality
  and are expected to be added directly to layouts, regions, and pages. Some
  examples include page titles, and special use menus.
{% endapply %}

{% include 'partials/grid-submenu.twig' with {
  heading: {
    content: 'Explore the various blocks',
    level: 2,
  },
  path: 'components/blocks',
} only %}
