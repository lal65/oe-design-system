---
title: 'Components - Atoms - Block Quotations'
meta:
  robots: 'noindex, nofollow'
  description: 'Block quotations are used to display extended quotations.'
page_subtitle_before: 'Atoms'
page_title: 'Block Quotations'
page_subtitle_after: 'Penn State World Campus'
menu_link_title: 'Block Quotations'
sort_order: 1
---
{% apply markdown_to_html %}
  Blockquotes are used to display extended quotations. They may optionally display an attribution.
{% endapply %}

{% include 'partials/component-docs.twig' with {
  installation: {
    npm: {
      package: '@oe/base',
    },
  },
  usage: {
    html: '<figure>
  <blockquote>Darkness cannot drive out darkness: only light can do that. Hate cannot drive out hate: only love can do that.</blockquote>
  <figcaption>—Martin Luther King Jr.</figcaption>
</figure>',
  }
} only %}

<br>
<br>
{% apply markdown_to_html %}
  ## Examples
{% endapply %}

<figure>
  <blockquote>Darkness cannot drive out darkness: only light can do that. Hate cannot drive out hate: only love can do that.</blockquote>
  <figcaption>—Martin Luther King Jr.</figcaption>
</figure>
<br>
<br>

{% set example_on_dark %}
  <figure>
    <blockquote>The question isn't who is going to let me; it's who is going to stop me.</blockquote>
    <figcaption>—Ayn Rand</figcaption>
  </figure>
{% endset %}
{% include '@oe/callout/callout.twig' with {
  background: 'blue-gradient',
  content: example_on_dark,
} only %}