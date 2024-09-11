---
title: 'Components - Layouts'
meta:
  robots: 'noindex, nofollow'
  description: 'Layouts are flexible, special purpose containers designed specifically for containing components. Examples of layouts include multi-column and grids.'
page_subtitle_before: 'Components'
page_title: 'Layouts'
page_subtitle_after: 'Penn State World Campus'
menu_link_title: 'Layouts'
sort_order: 5
---

{% apply markdown_to_html %}
Layouts are flexible, special purpose containers designed specifically for containing components. Examples of layouts include multi-column and grids.

## Explore the various layouts
{% endapply %}

{% set grid_items = [] %}
{% for item in get_menu_items()['components']['below']['components/layouts']['below'] %}
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

