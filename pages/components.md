---
title: 'Components'
meta:
  robots: 'noindex, nofollow'
  description: 'Explore the components that are available for use in the design system.'
page_subtitle_before: 'Design System'
page_title: 'Components'
page_subtitle_after: 'Penn State World Campus'
menu_link_title: 'Components'
sort_order: 5
---
{% apply markdown_to_html %}
An atomic design system breaks down a design into a hierarchy of reusable
components and defines classifications for said components. The World Campus
Design System has eight classifications of components, ranging from visual
styles to complete pages. Recommended uses for each component are documented in
this section.

## Explore the various component classifications
{% endapply %}
{% set grid_items = [] %}
{% for item in get_menu_items()['components']['below'] %}
  {% set grid_item %}
    {% include '@psu-ooe/navigation-tile/navigation-tile.twig' with {
      link: { url: item['url'], label: item['title'] },
      description: item['description'],
      chevron: true,
    } only %}
  {% endset %}
  {% set grid_items = grid_items|merge([grid_item]) %}
{% endfor %}
{% include '@psu-ooe/grid/grid.twig' with {
  items: grid_items
} only %}