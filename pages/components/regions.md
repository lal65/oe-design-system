---
title: 'Components - Regions'
meta:
  robots: 'noindex, nofollow'
  description: 'Regions are high level, semantic parts of a webpage. Examples include headers and footers.'
page_subtitle_before: 'Components'
page_title: 'Regions'
page_subtitle_after: 'Penn State World Campus'
menu_link_title: 'Regions'
sort_order: 6
---

{% apply markdown_to_html %}
Regions are high level, semantic parts of a webpage. Examples include headers and footers.

## Explore the various regions
{% endapply %}

{% set grid_items = [] %}
{% for item in get_menu_items()['components']['below']['components/regions']['below'] %}
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

