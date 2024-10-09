---
title: 'Components - Atoms - Email Inputs'
meta:
  robots: 'noindex, nofollow'
  description: 'Email inputs are a common form control for entering an email address.'
page_subtitle_before: 'Penn State World Campus'
page_title: 'Email Inputs'
page_subtitle_after: 'Design System Demo'
menu_link_title: 'Email Inputs'
sort_order: 0
---
{% apply markdown_to_html %}
  Email inputs are a common form control for entering an email address.
{% endapply %}

{% set installation %}
{% apply markdown_to_html %}
## Installation
Email input styles are currently provided through the input-email component.

### NPM
  ```bash
    npm install @psu-ooe/input-email
  ```
{% endapply %}
{% endset %}

{% set usage %}
{%- apply markdown_to_html -%}
## Usage
There is not yet a twig binding for email inputs.  As such, the only way to render one is through HTML.
{%- endapply -%}
<code>
<pre class="ds-example">
&lt;input type="email" /&gt;
</pre>
</code>
{% endset %}

{% include '@psu-ooe/tabs/tabs.twig' with {
tabs: [
{ id: 'email-installation'|clean_unique_id, title: 'Installation', content: installation },
{ id: 'email-usage'|clean_unique_id, title: 'Usage', content: usage },
],
} only %}
<br>
<br>
{% include 'partials/input-examples.twig' with {
  type: 'email',
  variations: [
    ['disabled'],
  ],
} only %}