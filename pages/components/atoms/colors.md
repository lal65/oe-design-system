---
title: 'Components - Atoms - Color Inputs'
meta:
  robots: 'noindex, nofollow'
  description: 'Color inputs are a common form control for selecting a color.'
page_subtitle_before: 'Penn State World Campus'
page_title: 'Color Inputs'
page_subtitle_after: 'Design System Demo'
menu_link_title: 'Color Inputs'
sort_order: 0
---
{% apply markdown_to_html %}
  Color inputs are a common form control for selecting a color.
{% endapply %}

{% set installation %}
  {% apply markdown_to_html %}
    ## Installation
    Color input styles are currently provided through the input-color component.

    ### NPM
    ```bash
      npm install @psu-ooe/input-color
    ```
  {% endapply %}
{% endset %}

{% set usage %}
  {%- apply markdown_to_html -%}
    ## Usage
      There is not yet a twig binding for color inputs.  As such, the only way to render one is through HTML.
  {%- endapply -%}
  <code>
    <pre class="ds-example">
&lt;input type="color" /&gt;
    </pre>
  </code>
{% endset %}

{% include '@psu-ooe/tabs/tabs.twig' with {
  tabs: [
    { id: 'color-installation'|clean_unique_id, title: 'Installation', content: installation },
    { id: 'color-usage'|clean_unique_id, title: 'Usage', content: usage },
  ],
} only %}
<br>
<br>
{% apply markdown_to_html %}
  ## Examples
  <input type="color" />
  <br>
  <br>
{% endapply %}

{% set example_on_dark %}
  <input type="color">
{% endset %}
{% include '@psu-ooe/callout/callout.twig' with {
  background: 'blue-gradient',
  content: example_on_dark,
} only %}
