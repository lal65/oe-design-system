---
title: 'Components - Atoms - Number Inputs'
meta:
  robots: 'noindex, nofollow'
  description: 'Number inputs are a common form control for entering a number.'
page_subtitle_before: 'Penn State World Campus'
page_title: 'Number Inputs'
page_subtitle_after: 'Design System Demo'
menu_link_title: 'Number Inputs'
sort_order: 0
---
{% apply markdown_to_html %}
Number inputs are a common form control for entering a number.
{% endapply %}

{% set installation %}
{% apply markdown_to_html %}
## Installation
Number input styles are currently provided through the input-number component.

    ### NPM
    ```bash
      npm install @psu-ooe/input-number
    ```
{% endapply %}
{% endset %}

{% set usage %}
{%- apply markdown_to_html -%}
## Usage
There is not yet a twig binding for number inputs.  As such, the only way to render one is through HTML.
{%- endapply -%}
<code>
<pre class="ds-example">
&lt;input type="number" /&gt;
</pre>
</code>
{% endset %}

{% include '@psu-ooe/tabs/tabs.twig' with {
tabs: [
{ id: 'number-installation'|clean_unique_id, title: 'Installation', content: installation },
{ id: 'number-usage'|clean_unique_id, title: 'Usage', content: usage },
],
} only %}
<br>
<br>
{% include 'partials/input-examples.twig' with {
  type: 'number',
  variations: [
    ['disabled'],
  ],
} only %}