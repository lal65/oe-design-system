---
title: 'Components - Atoms - Inputs'
meta:
  robots: 'noindex, nofollow'
  description: 'Inputs are a common form control that are assumed to be text inputs by default.'
page_subtitle_before: 'Penn State World Campus'
page_title: 'Inputs'
page_subtitle_after: 'Design System Demo'
menu_link_title: 'Inputs'
sort_order: 0
---
{% apply markdown_to_html %}
Inputs are a common form control that are assumed to be text inputs by default.
{% endapply %}

{% set installation %}
{% apply markdown_to_html %}
## Installation
Input styles are currently provided through the input-common component.

    ### NPM
    ```bash
      npm install @psu-ooe/input-common
    ```
{% endapply %}
{% endset %}

{% set usage %}
{%- apply markdown_to_html -%}
## Usage
There is not yet a twig binding for inputs.  As such, the only way to render one is through HTML.
{%- endapply -%}
<code>
<pre class="ds-example">
&lt;input /&gt;
</pre>
</code>
{% endset %}

{% include '@psu-ooe/tabs/tabs.twig' with {
tabs: [
{ id: 'input-installation'|clean_unique_id, title: 'Installation', content: installation },
{ id: 'input-usage'|clean_unique_id, title: 'Usage', content: usage },
],
} only %}
<br>
<br>
{% include 'partials/input-examples.twig' with {
  variations: [
    ['disabled'],
  ],
} only %}