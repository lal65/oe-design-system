---
title: 'Components - Atoms - Url Inputs'
meta:
  robots: 'noindex, nofollow'
  description: 'Url inputs are a common form control for selecting a url.'
page_subtitle_before: 'Atoms'
page_title: 'Url Inputs'
page_subtitle_after: 'Penn State World Campus'
menu_link_title: 'Url Inputs'
sort_order: 0
---
{% apply markdown_to_html %}
Url inputs are a common form control for selecting a url.
{% endapply %}

{% include 'partials/component-docs.twig' with {
  installation: {
    npm: {
      package: 'input-url',
    },
  },
  usage: {
    html: '<input type="url">',
  }
} only %}

<br>
<br>
{% include 'partials/input-examples.twig' with {
  type: 'url',
  variations: [
    ['disabled'],
  ],
} only %}