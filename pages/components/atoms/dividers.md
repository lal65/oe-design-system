---
title: 'Components - Atoms - Dividers'
meta:
  robots: 'noindex, nofollow'
  description: 'Dividers provide visual separation between sections of content.'
page_subtitle_before: 'Atoms'
page_title: 'Dividers'
page_subtitle_after: 'Penn State World Campus'
menu_link_title: 'Dividers'
sort_order: 0
---
{% apply markdown_to_html %}
  Dividers provide visual separation between sections of content.
{% endapply %}

{% include 'partials/component-docs.twig' with {
  installation: {
    npm: {
      package: 'divider',
    },
  },
  usage: {
    twig: '{% include "@oe/divider/divider.twig" with {
  variant: <variant>,
} only %}'
  }
} only %}
<br>
<br>
{% include 'partials/divider-examples.twig' %}
