---
title: 'Components - Atoms - Sprites'
meta:
  robots: 'noindex, nofollow'
  description: 'Sprites are imagery driven by powerful and performant SVGs.'
page_subtitle_before: 'Penn State World Campus'
page_title: 'Sprites'
page_subtitle_after: 'Design System Demo'
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
    twig: '{% include \'@psu-ooe/sprite/sprite.twig\' with {
  name: <code>
} only %}'
  }
} only %}
<br>
<br>
{% include 'partials/sprite-examples.twig' %}
