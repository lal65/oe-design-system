---
title: 'Components - Atoms - Call to action links'
meta:
  robots: 'noindex, nofollow'
  description: 'Call to action links special purpose link buttons.'
page_subtitle_before: 'Penn State World Campus'
page_title: 'Call to action links'
page_subtitle_after: 'Design System Demo'
menu_link_title: 'Call to action links'
sort_order: 0
---
{% apply markdown_to_html %}
  Call to action links special purpose link buttons.
{% endapply %}

{% include 'partials/component-docs.twig' with {
  installation: {
    npm: {
      package: 'cta',
    },
  },
  usage: {
    twig: '{% include "@psu-ooe/cta/cta-block.twig" with {
  label: "Call to action",
  url: "#",
} only %}'
  }
} only %}
<br>
<br>
{% include 'partials/cta-examples.twig' %}
