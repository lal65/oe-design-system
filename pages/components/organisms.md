---
title: 'Components - Organisms'
meta:
  robots: 'noindex, nofollow'
  description: 'Explore the components that are available for use in the design system.'
page_subtitle_before: 'Components'
page_title: 'Organisms'
page_subtitle_after: 'Penn State World Campus'
menu_link_title: 'Organisms'
sort_order: 2
---

{% apply markdown_to_html %}
Organisms in a design system are components that are made up of groups of molecules and/or other organisms. They are the building blocks of a user interface and are usually more complex than molecules but less complex than templates. Organisms are often reusable and can be combined with other organisms to create more complex user interfaces.## Explore the various molecules
{% endapply %}

{% set grid_items = [] %}
{% for item in get_menu_items()['components']['below']['components/molecules']['below'] %}
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

