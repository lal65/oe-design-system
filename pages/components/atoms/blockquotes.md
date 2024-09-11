---
title: 'Components - Atoms - Block Quotations'
meta:
  robots: 'noindex, nofollow'
  description: 'Block quotations are used to display extended quotations.'
page_subtitle_before: 'Penn State World Campus'
page_title: 'Block Quotations'
page_subtitle_after: 'Design System Demo'
menu_link_title: 'Block Quotations'
sort_order: 1
---
{% apply markdown_to_html %}
  Blockquotes are used to display extended quotations. They may optionally display an attribution.
{% endapply %}

{% set installation %}
  {% apply markdown_to_html %}
    ## Installation
    Blockquotes are currently provided through the design system base.
    ### NPM
    ```bash
      npm install @psu-ooe/base
    ```
  {% endapply %}
{% endset %}

{% set usage %}
  {% apply markdown_to_html %}
    ## Usage
    There is not yet a twig binding for blockquotes.  As such, the only way to render one is through HTML.
  {% endapply %}
  <code>
    <pre class="ds-example">
&lt;figure&gt;
  &lt;blockquote>Darkness cannot drive out darkness: only light can do that. Hate cannot drive out hate: only love can do that.&lt;/blockquote&gt;
  &lt;figcaption&gt;—Martin Luther King Jr.&lt;/figcaption&gt;
&lt;/figure&gt;
    </pre>
  </code>
{%- endset -%}

{% include '@psu-ooe/tabs/tabs.twig' with {
tabs: [
{ id: 'blockquote-installation'|clean_unique_id, title: 'Installation', content: installation },
{ id: 'blockquote-usage'|clean_unique_id, title: 'Usage', content: usage },
],
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
{% include '@psu-ooe/callout/callout.twig' with {
  background: 'blue-gradient',
  content: example_on_dark,
} only %}