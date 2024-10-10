---
title: 'Components - Atoms - Dividers'
meta:
  robots: 'noindex, nofollow'
  description: 'Dividers provide visual separation between sections of content.'
page_subtitle_before: 'Penn State World Campus'
page_title: 'Dividers'
page_subtitle_after: 'Design System Demo'
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
    twig: '{% include "@psu-ooe/divider/divider.twig" with {
  variant: <variant>,
} only %}'
  }
} only %}
<br>
<br>
{% include 'partials/divider-examples.twig' %}
