---
title: 'Components - Atoms - Password Inputs'
meta:
  robots: 'noindex, nofollow'
  description: 'Password inputs are a common form control for entering a password.'
page_subtitle_before: 'Atoms'
page_title: 'Password Inputs'
page_subtitle_after: 'Penn State World Campus'
menu_link_title: 'Password Inputs'
sort_order: 0
---
{% apply markdown_to_html %}
Password inputs are a common form control for entering a number.
{% endapply %}

{% include 'partials/component-docs.twig' with {
  installation: {
    npm: {
      package: 'input-password',
    },
  },
  usage: {
    html: '<input type="password">',
  }
} only %}
<br>
<br>
{% include 'partials/input-examples.twig' with {
  type: 'password',
  variations: [
    ['disabled'],
  ],
} only %}