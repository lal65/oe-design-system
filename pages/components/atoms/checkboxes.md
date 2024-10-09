---
title: 'Components - Atoms - Checkbox Inputs'
meta:
  robots: 'noindex, nofollow'
  description: 'Checkboxes are a common form control for selecting on or off state.'
page_subtitle_before: 'Penn State World Campus'
page_title: 'Checkbox Inputs'
page_subtitle_after: 'Design System Demo'
menu_link_title: 'Checkbox Inputs'
sort_order: 0
---
{% apply markdown_to_html %}
  Checkboxes are a common form control for selecting on or off state.
{% endapply %}

{% set installation %}
  {% apply markdown_to_html %}
    ## Installation
    Checkbox input styles are currently provided through the input-checkbox component.

    ### NPM
    ```bash
      npm install @psu-ooe/input-checkbox
    ```
  {% endapply %}
{% endset %}

{% set usage %}
  {%- apply markdown_to_html -%}
    ## Usage
      There is not yet a twig binding for checkbox inputs.  As such, the only way to render one is through HTML.
  {%- endapply -%}
  <code>
    <pre class="ds-example">
&lt;input type="checkbox" /&gt;
    </pre>
  </code>
{% endset %}

{% include '@psu-ooe/tabs/tabs.twig' with {
  tabs: [
    { id: 'checkbox-installation'|clean_unique_id, title: 'Installation', content: installation },
    { id: 'checkbox-usage'|clean_unique_id, title: 'Usage', content: usage },
  ],
} only %}
<br>
<br>
{% apply markdown_to_html %}
  ## Examples
  <input type="checkbox" />
  <br>
  <br>
{% endapply %}

{% set example_on_dark %}
  <input type="checkbox">
{% endset %}
{% include '@psu-ooe/callout/callout.twig' with {
  background: 'blue-gradient',
  content: example_on_dark,
} only %}
