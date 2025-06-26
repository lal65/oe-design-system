---
title: 'Components - Atoms - Fieldsets'
meta:
  robots: 'noindex, nofollow'
  description: 'Fieldsets are elements used to label and group several form controls.'
page_subtitle_before: 'Atoms'
page_title: 'Fieldsets'
page_subtitle_after: 'Penn State World Campus'
menu_link_title: 'Fieldsets'
sort_order: 0
---
{% apply markdown_to_html %}
  Fieldsets are elements used to label and group several form controls.
{% endapply %}

{% include 'partials/component-docs.twig' with {
  installation: {
    npm: {
      package: 'fieldset',
    },
  },
  usage: {
    html: '<fieldset>
  <legend>This is a fieldset.</legend>
  <p>There\'s nothing inside yet. @TODO: Fill it up.</p>
</fieldset>',
  }
} only %}

<br>
<br>
{% apply markdown_to_html %}
  ## Examples
{% endapply %}

<fieldset>
  <legend>This is a fieldset.</legend>
  <p>There's nothing inside yet. @TODO: Fill it up.</p>
</fieldset>
<br>
<br>

{% set example_on_dark %}
<fieldset>
  <legend>This is a fieldset.</legend>
  <p>There's nothing inside yet. @TODO: Fill it up.</p>
</fieldset>
{% endset %}
{% include '@oe/callout/callout.twig' with {
  background: 'blue-gradient',
  content: example_on_dark,
} only %}