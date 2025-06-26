---
title: 'Components - Atoms - Call to action links'
meta:
  robots: 'noindex, nofollow'
  description: 'Call to action links special purpose link buttons.'
page_subtitle_before: 'Atoms'
page_title: 'Call to action links'
page_subtitle_after: 'Penn State World Campus'
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
    twig: '{% include "@oe/cta/cta-block.twig" with {
  label: "Call to action",
  url: "#",
} only %}'
  }
} only %}
<br>
<br>
{% include 'partials/cta-examples.twig' %}
