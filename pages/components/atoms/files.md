---
title: 'Components - Atoms - File Inputs'
meta:
  robots: 'noindex, nofollow'
  description: 'File inputs are a common form control for uploading one or more files.'
page_subtitle_before: 'Penn State World Campus'
page_title: 'File Inputs'
page_subtitle_after: 'Design System Demo'
menu_link_title: 'File Inputs'
sort_order: 0
---
{% apply markdown_to_html %}
File inputs are a common form control for uploading one or more files.
{% endapply %}

{% set installation %}
{% apply markdown_to_html %}
## Installation
File input styles are currently provided through the input-file component.

### NPM
  ```bash
    npm install @psu-ooe/input-file
  ```
{% endapply %}
{% endset %}

{% set usage %}
{%- apply markdown_to_html -%}
## Usage
There is not yet a twig binding for file inputs.  As such, the only way to render one is through HTML.
{%- endapply -%}
<code>
<pre class="ds-example">
&lt;input type="file" /&gt;
</pre>
</code>
{% endset %}

{% include '@psu-ooe/tabs/tabs.twig' with {
tabs: [
{ id: 'file-installation'|clean_unique_id, title: 'Installation', content: installation },
{ id: 'file-usage'|clean_unique_id, title: 'Usage', content: usage },
],
} only %}
<br>
<br>
{% include 'partials/input-examples.twig' with {
  type: 'file',
  variations: [
    ['multiple'],
    ['disabled'],
    ['multiple', 'disabled'],
  ],
} only %}