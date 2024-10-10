---
title: 'Components - Atoms - Headings'
meta:
  robots: 'noindex, nofollow'
  description: 'Headings are used to logically group content under a common topic.'
page_subtitle_before: 'Atoms'
page_title: 'Headings'
page_subtitle_after: 'Penn State World Campus'
menu_link_title: 'Headings'
sort_order: 0
---
{% apply markdown_to_html %}
  Headings are used to logically group content under a common topic. They are
  hierarchical in nature and when looked at holistically, provide the user with
  an outline of the document. Correct use of headings is very important for
  providing non-visual users with an overview of the content present on a page.

  While various modifiers exist that can display headings in a number of ways,
  unless there is a very good reason to change the defaults, it is usually for
  the best if this is not done. The default heading styles make the visual size
  of each heading level match its relative position in the hierarchy, meaning
  that, for example, heading level 2 is visually larger and more predominant 
  than heading level 3.
{% endapply %}

{% set installation %}
  {% apply markdown_to_html %}
    ## Installation
    Install just like any other NPM package.
    ### NPM
    ```bash
    npm install @psu-ooe/heading
    ```
  {% endapply %}
{% endset %}

{% set usage %}
  {% apply markdown_to_html %}
    ## Usage
    Twig example:
  {% endapply %}
  <code><pre class="ds-example">{% verbatim %}
{% include '@psu-ooe/heading/heading.twig' with {
  content: 'The heading content',
} only %}{% endverbatim %}</pre></code>
{% endset %}

{% set documentation %}
  {% apply markdown_to_html %}
  ## Variables
  | Variable    | Type    | Required | Description                                                                 |
  |-------------|---------|----------|-----------------------------------------------------------------------------|
  | content     | string  | true     | The content to render within the heading. May contain arbitrary HTML.       |
  | level       | integer | false    | An integer, between 1 and 6 that denotes the heading level.  Defaults to 2. |
  | size        | string  | false    | Must match a documented size modifier.                                      |
  | align       | string  | false    | Must match a documented align modifier.                                     |
  | vspace      | string  | false    | Must match a documented vertical space modifier.                            |
  | position    | string  | false    | Must match a documented position modifier.                                  |
  | no_overline | boolean | false    | If specified, the heading will never render with an overline decoration.    |
  | reversed    | boolean | false    | If specified, the heading will render with an inverse color profile         |
  | subtle      | boolean | false    | If specified, the heading will render with a subtle look.                   |  
  {% endapply %}
{% endset %}

{% set modifiers %}
  {% apply markdown_to_html %}
    ## Modifiers
    Size, position, alignment, and vertical space may be customized.
    ### Size modifiers
    | Size    | Description                         |
      |---------|-------------------------------------|
    | xlarge  | This style looks like an &lt;h1&gt; |
    | large   | This style looks like an &lt;h2&gt; |
    | medium  | This style looks like an &lt;h3&gt; |
    | small   | This style looks like an &lt;h4&gt; |
    | xsmall  | This style looks like an &lt;h5&gt; |
    | 2xsmall | This style looks like an &lt;h6&gt; |
    
    ### Position modifiers
    | Modifier | Description                                                                                 |
      |----------|---------------------------------------------------------------------------------------------|
    | flush    | If specified, the heading will be shifted up to avoid extra space in the upper line-height. |
    
    ### Align modifiers
    | Modifier | Description                                       |
      |----------|---------------------------------------------------|
    | left     | If specified, the heading will be left aligned.   |
    | center   | If specified, the heading will be center aligned. |
    | right    | If specified, the heading will be right aligned.  |
    
    ### Vertical space modifiers
    | Modifier | Description                                               |
      |----------|-----------------------------------------------------------|
    | none     | If specified, the heading will have no margin bottom      |
    | small    | If specified, the heading will have a small margin bottom |
    | large    | If specified, the heading will have a large margin bottom |
  {% endapply %}
{% endset %}
{% set source_code %}
  {% apply markdown_to_html %}
    ### heading.twig
  {% endapply %}
  <code>
    <pre class="ds-example">
      {{- source('@psu-ooe/heading/heading.twig') -}}
    </pre>
  </code>
{% endset %}

{% include '@psu-ooe/tabs/tabs.twig' with {
  tabs: [
    { id: 'heading-installation'|clean_unique_id, title: 'Installation', content: installation },
    { id: 'heading-usage'|clean_unique_id, title: 'Usage', content: usage },
    { id: 'heading-variables'|clean_unique_id, title: 'Variables', content: documentation },
    { id: 'heading-modifiers'|clean_unique_id, title: 'Modifiers', content: modifiers },
    { id: 'heading-source'|clean_unique_id, title: 'Source code', content: source_code },
  ],
} only %}
<br>
<br>
{% apply markdown_to_html %}
  ## Examples
  ### Defaults
{% endapply %}
{{ example('{% include "@psu-ooe/heading/heading.twig" with {
  level: 1,
  content: "Heading 1: The quick brown fox jumps over the lazy dog",
} only %}', ['light', 'dark'])|raw }}
<br>
{{ example('{% include "@psu-ooe/heading/heading.twig" with {
  level: 2,
  content: "Heading 2: The quick brown fox jumps over the lazy dog",
} only %}', ['light', 'dark'])|raw }}
<br>
{{ example('{% include "@psu-ooe/heading/heading.twig" with {
  level: 3,
  content: "Heading 3: The quick brown fox jumps over the lazy dog",
} only %}', ['light', 'dark'])|raw }}
<br>
{{ example('{% include "@psu-ooe/heading/heading.twig" with {
  level: 4,
  content: "Heading 4: The quick brown fox jumps over the lazy dog",
} only %}', ['light', 'dark'])|raw }}
<br>

{{ example('{% include "@psu-ooe/heading/heading.twig" with {
  level: 5,
  content: "Heading 5: The quick brown fox jumps over the lazy dog",
} only %}', ['light', 'dark'])|raw }}
<br>

{{ example('{% include "@psu-ooe/heading/heading.twig" with {
  level: 6,
  content: "Heading 6: The quick brown fox jumps over the lazy dog",
} only %}', ['light', 'dark'])|raw }}
<br>

{% apply markdown_to_html %}
  ### Flushness
{% endapply %}
{{ example('
{% for level in range(1, 6) %}
  <div style="display: flex; flex-flow: row nowrap; gap: var(--text-element-vertical-space--default); margin-bottom: var(--text-element-vertical-space--default);">
    {% include "@psu-ooe/heading/heading.twig" with {
      content: "Should be flush with this box -->|",
      level: level,
      flush: true,
      no_overline: true,
    } only %}
    <div style="background: lightgrey;width:50px;height:50px;"></div>
  </div>
{% endfor %}
')|raw }}

{% apply markdown_to_html %}
### Vertical Spacing
{% endapply %}
{% for vspace in ["small", "medium", "large", "none"] %}
  {{ example('
    {% include "@psu-ooe/heading/heading.twig" with {
      content: "This heading has " ~ (vspace == "none" ? "no space" : ("a ' ~ vspace ~ ' amount of space")) ~ " under it",
      vspace: "' ~ vspace ~ '",
    } only %}
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
')|raw }}
<br>
{% endfor %}