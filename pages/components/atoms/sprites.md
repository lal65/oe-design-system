---
title: 'Components - Atoms - Sprites'
meta:
  robots: 'noindex, nofollow'
  description: 'Sprites are imagery driven by powerful and performant SVGs.'
page_subtitle_before: 'Atoms'
page_title: 'Sprites'
page_subtitle_after: 'Penn State World Campus'
menu_link_title: 'Sprites'
sort_order: 0
---
{% apply markdown_to_html %}
  Sprites are imagery driven by powerful and performant SVGs.
{% endapply %}

{% include 'partials/component-docs.twig' with {
  installation: {
    npm: {
      package: 'sprite',
    },
  },
  usage: {
    twig: '{% include \'@oe/sprite/sprite.twig\' with {
  name: <code>
} only %}'
  }
} only %}
<br>
<br>
{% include 'partials/sprite-examples.twig' %}
