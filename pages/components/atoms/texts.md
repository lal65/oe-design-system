---
title: 'Components - Atoms - Text Inputs'
meta:
  robots: 'noindex, nofollow'
  description: 'Text inputs are a common form control for entering generic single lines of text.'
page_subtitle_before: 'Penn State World Campus'
page_title: 'Text Inputs'
page_subtitle_after: 'Design System Demo'
menu_link_title: 'Text Inputs'
sort_order: 0
---
{% apply markdown_to_html %}
  Text inputs are a common form control for entering generic single lines of text.
{% endapply %}

{% include 'partials/component-docs.twig' with {
  installation: {
    npm: {
      package: 'input-text',
    },
  },
  usage: {
    html: '<input type="text">',
  }
} only %}
<br>
<br>
{% include 'partials/input-examples.twig' with {
  type: 'text',
  variations: [
    ['disabled'],
  ],
} only %}