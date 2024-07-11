---
title: 'Components'
meta:
  robots: 'index, follow'
  description: 'Explore the components that are available for use in the design system.'
page_subtitle_before: 'Design System'
page_title: 'Components'
page_subtitle_after: 'Penn State World Campus'
menu_link_title: 'Components'
sort_order: 3
---
{% apply markdown_to_html %}
An atomic design system breaks down a design into its most basic elements, starting with atoms. Atoms are the smallest building blocks of a design system, such as buttons, input fields, or icons. These atoms then combine to form molecules, which are slightly more complex components like a form or a navigation bar. Organisms are larger components made up of molecules and atoms, creating more complex structures like a hero section or footer. Blocks are collections of organisms that work together to form a section of a website or application, such as a header or sidebar. Regions are groupings of blocks that define specific areas of a design, like a main content area or a sidebar. Finally, pages are the highest level of the design system, encompassing all elements to create a complete layout or template for a website or application. By breaking designs down into these hierarchical levels, designers can create consistent and scalable systems for their projects.

## Explore the various component classifications
{% endapply %}
{% set grid_items = [] %}
{% for item in get_menu_items()['components']['below'] %}
  {% set grid_item %}
    {% include '@psu-ooe/navigation-tile/navigation-tile.twig' with {
      link: { url: item['url'], label: item['title'] }
    } only %}
  {% endset %}
  {% set grid_items = grid_items|merge([grid_item]) %}
{% endfor %}
{% include '@psu-ooe/grid/grid.twig' with {
  items: grid_items
} only %}