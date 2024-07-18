---
title: 'Components - Visual styles'
meta:
  robots: 'noindex, nofollow'
  description: 'Explore the components that are available for use in the design system.'
page_subtitle_before: 'Components'
page_title: 'Visual Styles'
page_subtitle_after: 'Penn State World Campus'
menu_link_title: 'Visual Styles'
sort_order: 0
---

{% apply markdown_to_html %}
  Visual styles in a design system refer to the predetermined set of design elements, such as typography, color palette, iconography, and spacing, that are used consistently across all digital interfaces and products within a brand or organization. These visual styles help create a cohesive and unified look and feel, ensuring consistency and brand recognition.
  Visual styles in a design system typically include:
  - Color palette: A defined set of colors that are used consistently throughout the design system for backgrounds, text, buttons, links, and other interface elements.
  - Typography: Consistent use of fonts, font sizes, line heights, and letter spacing for headings, subheadings, body text, and other text elements.
  - Iconography: A set of custom icons or icon libraries that are used consistently across the design system for buttons, navigation elements, symbols, and calls to action.
  - Spacing and layout: Consistent use of margins, padding, and grid systems to create a harmonious and balanced layout across all interfaces.
  - Visual hierarchy: Consistent use of hierarchy and emphasis to guide users' attention and help them navigate through the interface efficiently.
  By establishing and documenting these visual styles in a design system, designers and developers can ensure a seamless and cohesive user experience across different platforms and devices.
  ## Explore the visual aspects of the World Campus Design System
{% endapply %}

{% set grid_items = [] %}
  {% for item in get_menu_items()['components']['below']['components/visual-styles']['below'] %}
    {% set grid_item %}
      {% include '@psu-ooe/navigation-tile/navigation-tile.twig' with {
        link: {
          url: item['url'],
          label: item['title'],
        },
        description: item['description'],
      } only %}
    {% endset %}
  {% set grid_items = grid_items|merge([grid_item]) %}
{% endfor %}
{% include '@psu-ooe/grid/grid.twig' with {
  items: grid_items,
  columns: 2,
} only %}