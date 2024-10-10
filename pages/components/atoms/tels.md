---
title: 'Components - Atoms - Telephone Inputs'
meta:
  robots: 'noindex, nofollow'
  description: 'Telephone inputs are a common form control for entering telephone numbers.'
page_subtitle_before: 'Penn State World Campus'
page_title: 'Telephone Inputs'
page_subtitle_after: 'Design System Demo'
menu_link_title: 'Telephone Inputs'
sort_order: 0
---
{% apply markdown_to_html %}
  Telephone inputs are a common form control for entering telephone numbers.
{% endapply %}

{% include 'partials/component-docs.twig' with {
  installation: {
    npm: {
      package: 'input-tel',
    },
  },
  usage: {
    html: '<input type="tel">',
  }
} only %}
<br>
<br>
{% include 'partials/input-examples.twig' with {
  type: 'tel',
  variations: [
    ['disabled'],
  ],
} only %}