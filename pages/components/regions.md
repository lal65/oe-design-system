---
title: 'Components - Regions'
meta:
  robots: 'noindex, nofollow'
  description: 'Regions are high level, semantic parts of a webpage. Examples include headers and footers.'
page_subtitle_before: 'Components'
page_title: 'Regions'
page_subtitle_after: 'Penn State World Campus'
menu_link_title: 'Regions'
sort_order: 6
---

{% apply markdown_to_html %}
  Regions are high level, semantic parts of a webpage. Examples include headers
  and footers.
{% endapply %}

{% include 'partials/grid-submenu.twig' with {
  heading: {
    content: 'Explore the various regions',
    level: 2,
  },
  path: 'components/regions',
} only %}
