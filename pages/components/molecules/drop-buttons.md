---
title: 'Components - Molecules - Drop Buttons'
meta:
  robots: 'noindex, nofollow'
  description: 'Drop buttons are generic, mildly opinionated disclosure elements.'
page_subtitle_before: 'Molecules'
page_title: 'Drop Buttons'
page_subtitle_after: 'Penn State World Campus'
menu_link_title: 'Drop Buttons'
sort_order: 1
---
{% apply markdown_to_html %}
  Drop buttons are generic, mildly opinionated disclosure elements that consist
  of a toggle and a panel.  The toggle has no default styling, meaning that the
  caller must provide their own design.  Several more opinionated, higher order
  implementations using the drop-button component exist, such as the compact
  menu and compact search blocks.
{% endapply %}

{% set variables %}
  {% apply markdown_to_html %}
    | Variable       | Type    | Required | Description                                                                                                                         |
    |----------------|---------|----------|--------------------------------------------------------------|
    | toggle_content | string  | true     | The content to render within the drop-button toggle element. |
    | panel_content  | string  | false    | The content to render within the drop-button panel element.  |
    | panel_width    | enum    | false    | The width preset of the panel.                               |
    | panel_padding  | enum    | false    | The padding preset of the panel.                             |
  {% endapply %}
{% endset %}

{% set modifiers %}
  {% apply markdown_to_html %}
   ### Widths
   | Width | Description                                   |
   |-------|-----------------------------------------------|
   | wide  | Renders the drop-button panel at a wide size. |

   ### Paddings
   | Padding | Description                                       |
   |---------|---------------------------------------------------|
   | small   | Renders the drop-button panel with small padding. |
   | none    | Renders the drop-button panel with no padding.    |
    
   #### A note on the "none" padding option
   It is assumed that this option will be used when the panel content provides
   its own padding. This padding should be at minimum 1.414rem to avoid
   partial clipping with the drop-panel caret.
  {% endapply %}
{% endset %}
{% include 'partials/component-docs.twig' with {
  installation: {
    npm: {
      package: 'drop-button',
    },
  },
  usage: {
    twig: '
{% include "@psu-ooe/drop-button/drop-button.twig" with {
  toggle_content: <string>,
  panel_content: <string>,
  panel_width: <enum>,
  panel_padding: <enum>,
} only %}',
  },
  variables: variables,
  modifiers: modifiers,
} only %}

{% apply markdown_to_html %}
  <br>
  ## Examples
  No examples are available at this time.

  @TODO: Add examples.
{% endapply %}