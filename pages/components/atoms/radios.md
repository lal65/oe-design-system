---
title: 'Components - Atoms - Radio Inputs'
meta:
  robots: 'noindex, nofollow'
  description: 'Radio inputs are a common form control for choosing one option in a small set.'
page_subtitle_before: 'Atoms'
page_title: 'Radio Inputs'
page_subtitle_after: 'Penn State World Campus'
menu_link_title: 'Radio Inputs'
sort_order: 0
---
{% apply markdown_to_html %}
Radio inputs are a common form control for choosing one option in a small set.
{% endapply %}

{% include 'partials/component-docs.twig' with {
  installation: {
    npm: {
      package: 'input-radio',
    },
  },
  usage: {
    html: '<input type="radio">',
  }
} only %}
<br>
<br>
{% include 'partials/input-examples.twig' with {
  type: 'radio',
  variations: [
    ['disabled'],
  ],
} only %}`