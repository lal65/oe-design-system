---
title: 'Components - Molecules - Basic Tiles'
meta:
  robots: 'noindex, nofollow'
  description: 'Basic tiles are simple links that take on the appearance of tiles.'
page_subtitle_before: 'Molecules'
page_title: 'Basic Tiles'
page_subtitle_after: 'Penn State World Campus'
menu_link_title: 'Basic Tiles'
sort_order: 1
---
{% apply markdown_to_html %}
  Basic tiles are simple links that take on the appearance of tiles.

  ## Advanced Analytics Capabilities
  Basic tiles are able to be tagged with tracking placement and description
  data that is pushed into the datalayer when activated.  See the 
  [CTA Tracking](/components/utility/cta-tracking) documentation for more
  details.
{% endapply %}

{% set variables %}
  {% apply markdown_to_html %}
    | Variable             | Type    | Required | Description                                                             |
    |----------------------|---------|----------|-------------------------------------------------------------------------|
    | url                  | url     | true     | The URL of the tile.                                                    |
    | primary_label        | string  | true     | The primary label of the tile that renders most prominently.            |
    | secondary_label      | string  | false    | Optional content to render on a second line.                            |
    | tracking_placement   | string  | false    | A string that describes the location on the page where the tile exists. |
    | tracking_description | string  | false    | A string that uniquely identifies the purpose of the tile.              |
    | tracking_synchronous | boolean | false    | Should be set to true only if the link is to an external resource.      |
  {% endapply %}
{% endset %}

{% include 'partials/component-docs.twig' with {
  installation: {
    npm: {
      package: 'basic-tile',
    },
  },
  usage: {
    twig: '
{% include "@psu-ooe/basic-tile/basic-tile.twig" with {
  url: <url>,
  primary_label: <string>,
  secondary_label: <string>,
} only %}',
  },
  variables: variables,
  modifiers: modifiers,
  examples: [
    {
      label: 'Default', 
      content: '
{% include "@psu-ooe/basic-tile/basic-tile.twig" with {
  url: "#",
  primary_label: "Primary label",
  secondary_label: "Secondary label",
} only %}'
    },
    {
      label: 'Tracking Enabled', 
      content: '
{% include "@psu-ooe/basic-tile/basic-tile.twig" with {
  url: "#",
  primary_label: "Learn about the World Campus Student Government Association",
  secondary_label: "Clicks are tracked via datalayer",
  tracking_placement: "Example",
  tracking_description: "Student Government Association Interest",
  tracking_synchronous: false,
} only %}'
    },
  ]
} only %}