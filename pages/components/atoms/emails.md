---
title: 'Components - Atoms - Email Inputs'
meta:
  robots: 'noindex, nofollow'
  description: 'Email inputs are a common form control for entering an email address.'
page_subtitle_before: 'Penn State World Campus'
page_title: 'Email Inputs'
page_subtitle_after: 'Design System Demo'
menu_link_title: 'Email Inputs'
sort_order: 0
---
{% apply markdown_to_html %}
  Email inputs are a common form control for entering an email address.
{% endapply %}

{% include 'partials/component-docs.twig' with {
  installation: {
    npm: {
      package: 'input-email',
    },
  },
  usage: {
    html: '<input type="email">',
  }
} only %}
<br>
<br>
{% include 'partials/input-examples.twig' with {
  type: 'email',
  variations: [
    ['disabled'],
  ],
} only %}