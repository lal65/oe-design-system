---
title: 'Components - Atoms - Number Inputs'
meta:
  robots: 'noindex, nofollow'
  description: 'Number inputs are a common form control for entering a number.'
page_subtitle_before: 'Atoms'
page_title: 'Number Inputs'
page_subtitle_after: 'Penn State World Campus'
menu_link_title: 'Number Inputs'
sort_order: 0
---
{% apply markdown_to_html %}
Number inputs are a common form control for entering a number.
{% endapply %}

{% include 'partials/component-docs.twig' with {
  installation: {
    npm: {
      package: 'input-number',
    },
  },
  usage: {
    html: '<input type="number">',
  }
} only %}
<br>
<br>
{% include 'partials/input-examples.twig' with {
  type: 'number',
  variations: [
    ['disabled'],
  ],
} only %}