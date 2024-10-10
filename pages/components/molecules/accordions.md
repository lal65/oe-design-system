---
title: 'Components - Molecules - Accordions'
meta:
  robots: 'noindex, nofollow'
  description: 'Accordions are disclosure elements in which information is visible when open.'
page_subtitle_before: 'Penn State World Campus'
page_title: 'Accordions'
page_subtitle_after: 'Design System Demo'
menu_link_title: 'Accordions'
sort_order: 1
---
{% apply markdown_to_html %}
  Accordions are disclosure elements in which information is visible when open.
  While similar to details elements, accordions offer more flexibility with
  semantic aspects and animations.
{% endapply %}

{% set variables %}
  {% apply markdown_to_html %}
  | Variable    | Type    | Required | Description                                                                 |
  |-------------|---------|----------|-----------------------------------------------------------------------------|
  | toggle_content | string | true | The content to render within the accordion toggle element.
  | expandable_content     | string  | true     | The content to render within the accordion expandable element.       |
  | expanded       | boolean | false    | If set, the accordion will be expanded by default. |
  | label_underline        | boolean  | false    | If set, the accordion label will be underlined.                                      |
  | borderless       | boolean  | false    | If set, the accordion will render without borders.                                     |
  | heading_level      | string  | false    | If set, the accordion toggle will have heading semantics applied.                            |
  | heading_style    | string  | false    | If set, will override the heading style of the accordion toggle.                                  |
  | no_overline | boolean | false    | If specified, the heading will never render with an overline decoration.    |
  | reversed    | boolean | false    | If specified, the heading will render with an inverse color profile         |
  | subtle      | boolean | false    | If specified, the heading will render with a subtle look.                   |  
  {% endapply %}
{% endset %}

{% set modifiers %}
{% endset %}

{% include 'partials/component-docs.twig' with {
  installation: {
    npm: {
      package: 'accordion',
    },
  },
  usage: {
    twig: '
{% include "@psu-ooe/accordion/accordion.twig" with {
  id: "accordion-default",
  label: "Accordion label",
  expandable_content: "This is the accordion content."
} only %}',
  },
  variables: variables,
} only %}

<br>
<br>