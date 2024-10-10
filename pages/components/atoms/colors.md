---
title: 'Components - Atoms - Color Inputs'
meta:
  robots: 'noindex, nofollow'
  description: 'Color inputs are a common form control for selecting a color.'
page_subtitle_before: 'Penn State World Campus'
page_title: 'Color Inputs'
page_subtitle_after: 'Design System Demo'
menu_link_title: 'Color Inputs'
sort_order: 0
---
{% apply markdown_to_html %}
  Color inputs are a common form control for selecting a color.
{% endapply %}

{% include 'partials/component-docs.twig' with {
  installation: {
    npm: {
      package: 'input-color',
    },
  },
  usage: {
    html: '<input type="color">',
  }
} only %}
<br>
<br>
{% include 'partials/input-examples.twig' with {
  type: 'color',
  variations: [
    ['disabled'],
  ],
} only %}