---
title: 'Components - Atoms - Checkbox Inputs'
meta:
  robots: 'noindex, nofollow'
  description: 'Checkboxes are a common form control for selecting on or off state.'
page_subtitle_before: 'Atoms'
page_title: 'Checkbox Inputs'
page_subtitle_after: 'Penn State World Campus'
menu_link_title: 'Checkbox Inputs'
sort_order: 0
---
{% apply markdown_to_html %}
  Checkboxes are a common form control for selecting on or off state.
{% endapply %}

{% include 'partials/component-docs.twig' with {
  installation: {
    npm: {
      package: 'input-checkbox',
    },
  },
  usage: {
    html: '<input type="checkbox">',
  }
} only %}

<br>
<br>
{% include 'partials/input-examples.twig' with {
  type: 'checkbox',
  variations: [
    ['disabled'],
    ['checked'],
    ['checked', 'disabled'],
  ],
} only %}