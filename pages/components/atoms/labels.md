---
title: 'Components - Atoms - Labels'
meta:
  robots: 'noindex, nofollow'
  description: 'Labels are elements meant for captioning a user interface item.'
page_subtitle_before: 'Penn State World Campus'
page_title: 'Labels'
page_subtitle_after: 'Design System Demo'
menu_link_title: 'Labels'
sort_order: 0
---
{% apply markdown_to_html %}
  Labels are elements meant for captioning a user interface item.
{% endapply %}

{% include 'partials/component-docs.twig' with {
  installation: {
    npm: {
      package: 'label',
    },
  },
  usage: {
    html: '<label>Example label</label>',
  }
} only %}

<br>
<br>
{% apply markdown_to_html %}
  ## Examples
{% endapply %}

<label>Example label</label>
<br>
<br>

{% set example_on_dark %}
  <label>Example label</label>
{% endset %}
{% include '@psu-ooe/callout/callout.twig' with {
  background: 'blue-gradient',
  content: example_on_dark,
} only %}