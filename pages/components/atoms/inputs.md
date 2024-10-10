---
title: 'Components - Atoms - Inputs'
meta:
  robots: 'noindex, nofollow'
  description: 'Inputs are a common form control that are assumed to be text inputs by default.'
page_subtitle_before: 'Penn State World Campus'
page_title: 'Inputs'
page_subtitle_after: 'Design System Demo'
menu_link_title: 'Inputs'
sort_order: 0
---
{% apply markdown_to_html %}
Inputs are a common form control that are assumed to be text inputs by default.
{% endapply %}

{% include 'partials/component-docs.twig' with {
  installation: {
    npm: {
      package: 'input-common',
    },
  },
  usage: {
    html: '<input>',
  }
} only %}
<br>
<br>
{% include 'partials/input-examples.twig' with {
  variations: [
    ['disabled'],
  ],
} only %}