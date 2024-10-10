---
title: 'Components - Atoms - Date Inputs'
meta:
  robots: 'noindex, nofollow'
  description: 'Date inputs are a common form control for selecting a date.'
page_subtitle_before: 'Atoms'
page_title: 'Date Inputs'
page_subtitle_after: 'Penn State World Campus'
menu_link_title: 'Date Inputs'
sort_order: 0
---
{% apply markdown_to_html %}
Date inputs are a common form control for selecting a date.
{% endapply %}

{% include 'partials/component-docs.twig' with {
  installation: {
    npm: {
      package: 'input-date',
    },
  },
  usage: {
    html: '<input type="date">',
  }
} only %}

<br>
<br>
{% include 'partials/input-examples.twig' with {
  type: 'date',
  variations: [
    ['disabled'],
  ],
} only %}