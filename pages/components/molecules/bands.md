---
title: 'Components - Molecules - Bands'
meta:
  robots: 'noindex, nofollow'
  description: 'Bands are simple containers that are meant to be stacked inside sticky panels.'
page_subtitle_before: 'Molecules'
page_title: 'Bands'
page_subtitle_after: 'Penn State World Campus'
menu_link_title: 'Bands'
sort_order: 1
---
{% apply markdown_to_html %}
  Bands are simple containers that are meant to be stacked inside sticky
  panels.
{% endapply %}

{% set variables %}
  {% apply markdown_to_html %}
    | Variable   | Type   | Required | Description                                                                                                                         |
    |------------|--------|----------|-------------------------------------------------------------------------------------------------------------------------------------|
    | content    | string | true     | The content to render inside the container.                                                                                         |
    | background | string | false    | May match a documented background modifier (below). If not overridden, a default background color is applied.                       |
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
{% include "@psu-ooe/band/band.twig" with {
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
{% include "@psu-ooe/band/band.twig" with {
  content: "Primary content displayed with default padding.",
} only %}'
    },
    {
      unwrapped: true,
      label: 'Compact', 
      content: '
{% include "@psu-ooe/band/band.twig" with {
  content: "Primary content displayed with compact padding.",
  padding: "compact",
} only %}'
    },
    {
      unwrapped: true,
      label: 'No padding', 
      content: '
{% include "@psu-ooe/band/band.twig" with {
  content: "Primary content displayed with no padding.",
  padding: "none",
} only %}'
    },
    {
      unwrapped: true,
      label: 'Secondary', 
      content: '
{% include "@psu-ooe/band/band.twig" with {
  content: "Secondary content displayed with default padding.",
  background: "secondary",
} only %}'
    },
    {
      unwrapped: true,
      label: 'Hub geometric', 
      content: '
{% include "@psu-ooe/band/band.twig" with {
  content: "Hub geometric content displayed with default padding.",
  background: "hub-geometric",
} only %}'
    },
  ]
} only %}