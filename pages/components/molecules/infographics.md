---
title: 'Components - Molecules - Infographics'
meta:
  robots: 'noindex, nofollow'
  description: 'Infographics are bold, visually appealing representations of discrete pieces of information.'
page_subtitle_before: 'Molecules'
page_title: 'Infographics'
page_subtitle_after: 'Penn State World Campus'
menu_link_title: 'Infographics'
sort_order: 1
---
{% apply markdown_to_html %}
  Infographics are bold, visually appealing representations of discrete pieces
  of information. They consist of emphasis, preliminary, and primary text
  parts.
{% endapply %}

{% set variables %}
  {% apply markdown_to_html %}
    | Variable    | Type   | Required | Description                                                                                                            |
    |-------------|--------|----------|------------------------------------------------|
    | emphasis    | string | false    | The most bold and impactful visual to display. |
    | preliminary | string | false    | Supporting context for the primary message.    |
    | primary     | string | false    | The primary message to display.                |
  {% endapply %}
{% endset %}

{% include 'partials/component-docs.twig' with {
  installation: {
    npm: {
      package: 'infographic',
    },
  },
  usage: {
    twig: '
{% include "@oe/infographic/infographic.twig" with {
  emphasis: <string>,
  preliminary: <string>,
  primary: <string>,
} only %}',
  },
  variables: variables,
  examples: [
    {
      label: 'Default', 
      content: '
{% include "@oe/infographic/infographic.twig" with {
  emphasis: "16",
  preliminary: "Liberal arts and communications",
  primary: "Degrees and Certificates",
} only %}'
    },
    {
      label: 'No emphasis', 
      content: '
{% include "@oe/infographic/infographic.twig" with {
  preliminary: "Liberal arts and communications",
  primary: "Degrees and Certificates",
} only %}'
    },
    {
      label: 'No preliminary', 
      content: '
{% include "@oe/infographic/infographic.twig" with {
  emphasis: "16",
  primary: "Degrees and Certificates",
} only %}'
    },
    {
      label: 'No primary', 
      content: '
{% include "@oe/infographic/infographic.twig" with {
  emphasis: "16",
  preliminary: "Liberal arts and communications",
} only %}'
    },
    {
      label: 'Only emphasis', 
      content: '
{% include "@oe/infographic/infographic.twig" with {
  emphasis: "16",
} only %}'
    },
    {
      label: 'Only preliminary', 
      content: '
{% include "@oe/infographic/infographic.twig" with {
  preliminary: "Liberal arts and communications",
} only %}'
    },
    {
      label: 'Only primary', 
      content: '
{% include "@oe/infographic/infographic.twig" with {
  primary: "Degrees and Certificates",
} only %}'
    },
  ]
} only %}
