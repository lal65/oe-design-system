---
title: 'Components - Atoms - Legends'
meta:
  robots: 'noindex, nofollow'
  description: 'Legends are elements meant for captioning a fieldset.'
page_subtitle_before: 'Atoms'
page_title: 'Legends'
page_subtitle_after: 'Penn State World Campus'
menu_link_title: 'Legends'
sort_order: 0
---
{% apply markdown_to_html %}
  Legends are elements meant for captioning a fieldset.
{% endapply %}

{% include 'partials/component-docs.twig' with {
  installation: {
    npm: {
      package: 'legend',
    },
  },
  usage: {
    html: '<legend>Example legend</legend>',
  }
} only %}

<br>
<br>
{% apply markdown_to_html %}
  ## Examples
{% endapply %}

<legend>Example legend</legend>
<br>
<br>

{% set example_on_dark %}
  <legend>Example legend</legend>
{% endset %}
{% include '@psu-ooe/callout/callout.twig' with {
  background: 'blue-gradient',
  content: example_on_dark,
} only %}