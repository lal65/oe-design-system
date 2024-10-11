---
title: 'Components - Molecules - Callouts'
meta:
  robots: 'noindex, nofollow'
  description: 'Callouts are containers that are meant to be used in limited width contexts.'
page_subtitle_before: 'Molecules'
page_title: 'Callouts'
page_subtitle_after: 'Penn State World Campus'
menu_link_title: 'Callouts'
sort_order: 1
---
{% apply markdown_to_html %}
  Callouts are containers that are meant to be used in limited width contexts.
{% endapply %}

{% set variables %}
  {% apply markdown_to_html %}
    | Variable           | Type   | Required | Description                                                           |
    |--------------------|--------|----------|-----------------------------------------------------------------------|
    | content            | string | true     | The content to render within the heading. May contain arbitrary HTML. |
    | background         | string | false    | Must match a documented background modifier (below).                  |
    | shadow             | string | false    | Must match a documented shadow modifier (below).                      |
    | width              | string | false    | Must match a documented width modifier (below).                       |
    | padding_vertical   | string | false    | Must match a documented padding vertical modifier (below).            |
    | padding_horizontal | string | false    | Must match a documented padding vertical modifier (below).            |
  {% endapply %}
{% endset %}

{% set modifiers %}
  {% apply markdown_to_html %}

    ### Backgrounds

    | Size          | Description                                               |
    |---------------|-----------------------------------------------------------|
    | white         | If specified, renders a white background variant.         |
    | light-grey    | If specified, renders a light grey background variant.    |
    | blue-gradient | If specified, renders a blue gradient background variant. |
    | blue          | If specified, renders a blue background variant.          |
    
    ### Shadows

    | Shadow   | Description                              |
    |----------|------------------------------------------|
    | standard | If specified, renders a standard shadow. |
    
    ### Widths

    | Modifier | Description                                                  |
    |----------|--------------------------------------------------------------|
    | narrow   | If specified, content will be constrained to a narrow width. |
    
    ### Vertical paddings

    | Modifier          | Description                                                                               |
    |-------------------|-------------------------------------------------------------------------------------------|
    | xsmall            | If specified, an extra small amount of padding is used.                                   |
    | small             | If specified, a small amount of padding is used.                                          |
    | small-percentage  | If specified, a small amount of variable padding is used, clamped by two sentinel values. |
    | medium-percentage | If specified, a medium amount of variable padding is used, clamped by two sentinel values. |
    | large-percentage  | If specified, a large amount of variable padding is used, clamped by two sentinel values. |
    
    ### Horizontal paddings

    | Modifier          | Description                                                                               |
    |-------------------|-------------------------------------------------------------------------------------------|
    | small-percentage  | If specified, a small amount of variable padding is used, clamped by two sentinel values. |
    | medium-percentage | If specified, a medium amount of variable padding is used, clamped by two sentinel values. |
    | large-percentage  | If specified, a large amount of variable padding is used, clamped by two sentinel values. |
  {% endapply %}
{% endset %}

{% include 'partials/component-docs.twig' with {
  installation: {
    npm: {
      package: 'callout',
    },
  },
  usage: {
    twig: '
{% include "@psu-ooe/callout/callout.twig" with {
  content: "This is the callout content."
} only %}',
  },
  variables: variables,
  modifiers: modifiers,
  examples: [
    {
      unwrapped: true,
      label: 'Default', 
      content: '
{% include "@psu-ooe/callout/callout.twig" with {
  content: "This is a callout with a transparent background.",
} only %}'
    },
    {
      unwrapped: true,
      label: 'Blue', 
      content: '
{% include "@psu-ooe/callout/callout.twig" with {
  content: "This is a callout with a blue background.",
  background: "blue",
} only %}'
    },
    {
      unwrapped: true,
      label: 'Blue gradient', 
      content: '
{% include "@psu-ooe/callout/callout.twig" with {
  content: "This is a callout with a blue gradient background.",
  background: "blue-gradient",
} only %}'
    },
    {
      unwrapped: true,
      label: 'Light grey', 
      content: '
{% include "@psu-ooe/callout/callout.twig" with {
  content: "This is a callout with a light grey background.",
  background: "light-grey",
} only %}'
    },
    {
      unwrapped: true,
      label: 'White', 
      content: '
{% include "@psu-ooe/callout/callout.twig" with {
  content: "This is a callout with a white background.",
  background: "white",
} only %}'
    },
    {
      unwrapped: true,
      label: 'Large percentage padding', 
      content: '
{% include "@psu-ooe/callout/callout.twig" with {
  content: "This is a callout with large percentage based padding.",
  background: "light-grey",
  padding_horizontal: "large-percentage",
  padding_vertical: "large-percentage",
} only %}'
    },
    {
      unwrapped: true,
      label: 'Medium percentage padding', 
      content: '
{% include "@psu-ooe/callout/callout.twig" with {
  content: "This is a callout with medium percentage based padding.",
  background: "light-grey",
  padding_horizontal: "medium-percentage",
  padding_vertical: "medium-percentage",
} only %}'
    },
    {
      unwrapped: true,
      label: 'Small percentage padding', 
      content: '
{% include "@psu-ooe/callout/callout.twig" with {
  content: "This is a callout with medium percentage based padding.",
  background: "light-grey",
  padding_horizontal: "small-percentage",
  padding_vertical: "small-percentage",
} only %}'
    },
    {
      unwrapped: true,
      label: 'Small vertical padding', 
      content: '
{% include "@psu-ooe/callout/callout.twig" with {
  content: "This is a callout with small vertical padding.",
  background: "light-grey",
  padding_vertical: "small",
} only %}'
    },
    {
      unwrapped: true,
      label: 'Extra small vertical padding', 
      content: '
{% include "@psu-ooe/callout/callout.twig" with {
  content: "This is a callout with extra small vertical padding.",
  background: "light-grey",
  padding_vertical: "xsmall",
} only %}'
    },
    {
      unwrapped: true,
      label: 'Standard Shadow', 
      content: '
{% include "@psu-ooe/callout/callout.twig" with {
  content: "This is a callout with a standard shadow.",
  shadow: "standard",
} only %}'
    },
    {
      unwrapped: true,
      label: 'Narrow width', 
      content: '
{% include "@psu-ooe/callout/callout.twig" with {
  content: "This is a callout with a narrow width.",
  width: "narrow",
} only %}'
    },
  ]
} only %}