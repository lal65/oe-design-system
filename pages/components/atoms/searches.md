---
title: 'Components - Atoms - Search Inputs'
meta:
  robots: 'noindex, nofollow'
  description: 'Search inputs are a common form control for entering search terms.'
page_subtitle_before: 'Penn State World Campus'
page_title: 'Search Inputs'
page_subtitle_after: 'Design System Demo'
menu_link_title: 'Search Inputs'
sort_order: 0
---
{% apply markdown_to_html %}
Search inputs are a common form control for entering search terms.
{% endapply %}

{% include 'partials/component-docs.twig' with {
  installation: {
    npm: {
      package: 'input-search',
    },
  },
  usage: {
    html: '<input type="search">',
  }
} only %}
<br>
<br>
{% include 'partials/input-examples.twig' with {
  type: 'search',
  variations: [
    ['disabled'],
  ],
} only %}