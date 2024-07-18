---
title: 'Components - Atoms - Headings'
meta:
  robots: 'noindex, nofollow'
  description: 'Headings are used to logically group content under a common topic.'
page_subtitle_before: 'Penn State World Campus'
page_title: 'Headings'
page_subtitle_after: 'Design System Demo'
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

{% set documentation %}
  {% apply markdown_to_html %}
  ## Variables
  | Variable     | Type    | Required | Description                                                                 |
  |--------------|---------|----------|-----------------------------------------------------------------------------|
  | content      | string  | true     | The content to render within the heading. May contain arbitrary HTML.       |
  | level        | integer | false    | An integer, between 1 and 6 that denotes the heading level.  Defaults to 2. |
  | size         | string  | false    | Must match a documented size modifier (below).                              |
  | align        | string  | false    | Must match a documented align modifier (below).                             |
  | vspace       | string  | false    | Must match a documented vertical space modifier (below).                    |
  | position     | string  | false    | Must match a documented position modifier (below).                          |
  | no_overline  | boolean | false    | If specified, the heading will never render with an overline decoration.    |
  | reversed     | boolean | false    | If specified, the heading will render with an inverse color profile         |
  | subtle       | boolean | false    | If specified, the heading will render with a subtle look.                   |
  
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
  <code>
    <pre class="ds-example">
      {{- source('@psu-ooe/heading/heading.twig') -}}
    </pre>
  </code>
{% endset %}
{% include '@psu-ooe/tabs/tabs.twig' with {
  tabs: [
    { id: 'heading-variables'|clean_unique_id, title: 'Documentation', content: documentation },
    { id: 'heading-source'|clean_unique_id, title: 'Source code', content: source_code },
  ],
} only %}