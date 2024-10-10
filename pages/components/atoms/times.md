---
title: 'Components - Atoms - Time Inputs'
meta:
  robots: 'noindex, nofollow'
  description: 'Time inputs are a common form control for selecting a time.'
page_subtitle_before: 'Atoms'
page_title: 'Time Inputs'
page_subtitle_after: 'Penn State World Campus'
menu_link_title: 'Time Inputs'
sort_order: 0
---
{% apply markdown_to_html %}
Time inputs are a common form control for selecting a time.
{% endapply %}

{% include 'partials/component-docs.twig' with {
  installation: {
    npm: {
      package: 'input-time',
    },
  },
  usage: {
    html: '<input type="time">',
  }
} only %}

<br>
<br>
{% include 'partials/input-examples.twig' with {
  type: 'time',
  variations: [
    ['disabled'],
  ],
} only %}