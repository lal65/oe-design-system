---
title: 'Components - Molecules - Intro Forms'
meta:
  robots: 'noindex, nofollow'
  description: 'Intro Forms are opinionated containers feature decorative images, a heading, text, and form elements.'
page_subtitle_before: 'Molecules'
page_title: 'Intro Forms'
page_subtitle_after: 'Penn State World Campus'
menu_link_title: 'Intro Forms'
sort_order: 1
---
{% apply markdown_to_html %}
  Intro Forms are opinionated containers feature a decorative image, heading,
  text, and form elements. They are expected to be used in full-width contexts
  and are design-optimized for forms that consist of 3 to 5 visible fields at
  any given point in time. Multiple images may be provided in order to serve a
  randomized image every page view.
{% endapply %}

{% set variables %}
  {% apply markdown_to_html %}
    | Variable   | Type   | Required | Description                                                                                                                         |
    |------------|--------|----------|-------------------------------------------------------------------------------------------------------------------------------------|
    | form    | html | true     | The form to render.                                                                                         |
    | title | string | false    | May match a documented background modifier (below). If not overridden, a default background color is applied.                       |
    | heading_level | string | 
    | padding    | string | false    | May match a documented padding modifier (below). If not overridden, a default amount of vertical padding is added to the container. |
  {% endapply %}
{% endset %}

{% set modifiers %}
  {% apply markdown_to_html %}

    ### Backgrounds

    | Background    | Description                                      |
    |---------------|--------------------------------------------------|
    | secondary     | Display the band in a secondary color profile    |
    | hub-geometric | Display the band with a hub geometric background |

    ### Paddings

    | Padding | Description                                                    |
    |---------|----------------------------------------------------------------|
    | compact | Applies a smaller amount of vertical padding to the container. |
    | none    | Applies no vertical padding to the container.                  |
  {% endapply %}
{% endset %}

{% include 'partials/component-docs.twig' with {
  installation: {
    npm: {
      package: 'band',
    },
  },
  usage: {
    twig: '
{% include "@oe/band/band.twig" with {
  content: "This is the band content."
} only %}',
  },
  variables: variables,
  modifiers: modifiers,
  examples: [
    {
      unwrapped: true,
      label: 'Default', 
      content: '
{% include "@oe/band/band.twig" with {
  content: "Primary content displayed with default padding.",
} only %}'
    },
    {
      unwrapped: true,
      label: 'Compact', 
      content: '
{% include "@oe/band/band.twig" with {
  content: "Primary content displayed with compact padding.",
  padding: "compact",
} only %}'
    },
    {
      unwrapped: true,
      label: 'No padding', 
      content: '
{% include "@oe/band/band.twig" with {
  content: "Primary content displayed with no padding.",
  padding: "none",
} only %}'
    },
    {
      unwrapped: true,
      label: 'Secondary', 
      content: '
{% include "@oe/band/band.twig" with {
  content: "Secondary content displayed with default padding.",
  background: "secondary",
} only %}'
    },
    {
      unwrapped: true,
      label: 'Hub geometric', 
      content: '
{% include "@oe/band/band.twig" with {
  content: "Hub geometric content displayed with default padding.",
  background: "hub-geometric",
} only %}'
    },
  ]
} only %}