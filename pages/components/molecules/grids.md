---
title: 'Components - Molecules - Grids'
meta:
  robots: 'noindex, nofollow'
  description: 'Grids are simple layouts that allow content to be displayed in a set number of columns.'
page_subtitle_before: 'Molecules'
page_title: 'Grids'
page_subtitle_after: 'Penn State World Campus'
menu_link_title: 'Grids'
sort_order: 1
---
{% apply markdown_to_html %}
  Grids are simple layouts that allow content to be displayed in a set number
  of columns.  Unlike multi-column layouts, empty grid items will still take up
  space and will not automatically collapse.
{% endapply %}

{% set variables %}
  {% apply markdown_to_html %}
    | Variable | Type    | Required | Description                                                                                                            |
    |----------|---------|----------|-------------------------------------------------------------------------------------------------|
    | items    | array   | true     | The items to display within the grid.                                                           |
    | columns  | integer | false    | The number of columns to use in the grid, defaults to 3.  Must be between 1 and 4 if specified. |
  {% endapply %}
{% endset %}

{% include 'partials/component-docs.twig' with {
  installation: {
    npm: {
      package: 'grid',
    },
  },
  usage: {
    twig: '
{% include "@oe/grid/grid.twig" with {
  items: <array>,
  columns: <integer>,
} only %}',
  },
  variables: variables,
  examples: [
    {
      label: 'One column', 
      content: '
{% include "@oe/grid/grid.twig" with {
  items: ["item 1", "item 2", "item 3", "item 4"],
  columns: 1,
} only %}'
    },
    {
      label: 'Two column', 
      content: '
{% include "@oe/grid/grid.twig" with {
  items: ["item 1", "item 2", "item 3", "item 4"],
  columns: 2,
} only %}'
    },
    {
      label: 'Three column', 
      content: '
{% include "@oe/grid/grid.twig" with {
  items: ["item 1", "item 2", "item 3", "item 4"],
  columns: 3,
} only %}'
    },
    {
      label: 'Four column', 
      content: '
{% include "@oe/grid/grid.twig" with {
  items: ["item 1", "item 2", "item 3", "item 4"],
  columns: 4,
} only %}'
    },
  ]
} only %}
