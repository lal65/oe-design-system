---
title: 'Components - Atoms - Selects'
meta:
  robots: 'noindex, nofollow'
  description: 'Select elements are a common form control for choosing one or more options in a set.'
page_subtitle_before: 'Atoms'
page_title: 'Selects'
page_subtitle_after: 'Penn State World Campus'
menu_link_title: 'Selects'
sort_order: 0
---
{% apply markdown_to_html %}
  Selects elements are a common form control for choosing one or more options in a set.
{% endapply %}

{% include 'partials/component-docs.twig' with {
  installation: {
    npm: {
      package: 'select',
    },
  },
  usage: {
    html: '<select>
  <option value="1">First option</option>
  <option value="2">Second option</option>
  <option value="3">Third option</option>
</select>',
  }
} only %}
<br>
<br>
{% set examples %}
  <label>Select
    <select>
      <option value="1">First option</option>
      <option value="2">Second option</option>
      <option value="3">Third option</option>
    </select>
  </label>
  <br><br>
  <label>Select (error)
    <select class="error">
      <option value="1">First option</option>
      <option value="2">Second option</option>
      <option value="3">Third option</option>
    </select>
  </label>
  <br><br>
  <label>Select (disabled)
    <select disabled>
      <option value="1">First option</option>
      <option value="2">Second option</option>
      <option value="3">Third option</option>
    </select>
  </label>
  <br><br>
  <label>Select (multiple)
    <select multiple>
      <option value="1">First option</option>
      <option value="2">Second option</option>
      <option value="3">Third option</option>
    </select>
  </label>
  <br><br>
  <label>Select (multiple, error)
    <select multiple class="error">
      <option value="1">First option</option>
      <option value="2">Second option</option>
      <option value="3">Third option</option>
    </select>
  </label>
  <br><br>
  <label>Select (multiple, disabled)
    <select multiple disabled>
      <option value="1">First option</option>
      <option value="2">Second option</option>
      <option value="3">Third option</option>
    </select>
  </label>{% endset %}

{{ examples }}
<br>
<br>
{% include '@oe/callout/callout.twig' with {
  background: 'blue-gradient',
  content: examples,
} only %}