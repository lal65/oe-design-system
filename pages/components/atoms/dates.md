---
title: 'Components - Atoms - Date Inputs'
meta:
  robots: 'noindex, nofollow'
  description: 'Date inputs are a common form control for selecting a date.'
page_subtitle_before: 'Penn State World Campus'
page_title: 'Date Inputs'
page_subtitle_after: 'Design System Demo'
menu_link_title: 'Date Inputs'
sort_order: 0
---
{% apply markdown_to_html %}
Date inputs are a common form control for selecting a date.
{% endapply %}

{% set installation %}
{% apply markdown_to_html %}
  ## Installation
  Date input styles are currently provided through the input-date component.

  ### NPM
  ```bash
    npm install @psu-ooe/input-date
  ```
{% endapply %}
{% endset %}

{% set usage %}
{%- apply markdown_to_html -%}
## Usage
There is not yet a twig binding for date inputs.  As such, the only way to render one is through HTML.
{%- endapply -%}
<code>
<pre class="ds-example">
&lt;input type="date" /&gt;
</pre>
</code>
{% endset %}

{% include '@psu-ooe/tabs/tabs.twig' with {
tabs: [
{ id: 'date-installation'|clean_unique_id, title: 'Installation', content: installation },
{ id: 'date-usage'|clean_unique_id, title: 'Usage', content: usage },
],
} only %}
<br>
<br>
{% apply markdown_to_html %}
## Examples
  <input type="date" />
  <br>
  <br>
{% endapply %}

{% set example_on_dark %}
<input type="date">
{% endset %}
{% include '@psu-ooe/callout/callout.twig' with {
background: 'blue-gradient',
content: example_on_dark,
} only %}
