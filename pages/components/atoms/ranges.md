---
title: 'Components - Atoms - Range Inputs'
meta:
  robots: 'noindex, nofollow'
  description: 'Range inputs are a common form control for a value between a min and max.'
page_subtitle_before: 'Atoms'
page_title: 'Range Inputs'
page_subtitle_after: 'Penn State World Campus'
menu_link_title: 'Range Inputs'
sort_order: 0
---
{% apply markdown_to_html %}
Range inputs are a common form control for a value between a min and max.
{% endapply %}

{% include 'partials/component-docs.twig' with {
  installation: {
    npm: {
      package: 'input-range',
    },
  },
  usage: {
    html: '<input type="range">',
  }
} only %}
<br>
<br>
{% include 'partials/input-examples.twig' with {
  type: 'range',
  variations: [
    ['disabled'],
  ],
} only %}