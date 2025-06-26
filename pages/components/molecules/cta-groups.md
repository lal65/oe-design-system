---
title: 'Components - Molecules - Call to action groups'
meta:
  robots: 'noindex, nofollow'
  description: 'Call to action groups are specialized containers for call to action buttons.'
page_subtitle_before: 'Molecules'
page_title: 'Call to action groups'
page_subtitle_after: 'Penn State World Campus'
menu_link_title: 'Call to action groups'
sort_order: 1
---
{% apply markdown_to_html %}
  Call to action groups are specialized containers for call to action buttons.
{% endapply %}

{% set variables %}
  {% apply markdown_to_html %}
    | Variable      | Type    | Required | Description                                                                                                                         |
    |---------------|---------|----------|------------------------------------------------------------------------|
    | ctas          | array   | true     | The array of call to action buttons to display in this group.          |
    | align_right   | boolean | false    | If toggled, buttons will be right aligned in the container.            |
    | expand_to_fit | boolean | false    | If toggled, buttons will proportionately expand to fill the container. |
  {% endapply %}
{% endset %}


{% include 'partials/component-docs.twig' with {
  installation: {
    npm: {
      package: 'cta',
    },
  },
  usage: {
    twig: '
{% include "@oe/cta/cta-group.twig" with {
  ctas: <array>,
  align_right: <boolean>,
  expand_to_fit: <boolean>,
} only %}',
  },
  variables: variables,
} only %}

{% apply markdown_to_html %}
  ## Examples
  No examples are available at this time.
{% endapply %}