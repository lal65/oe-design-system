---
title: 'Components - Pages'
meta:
  robots: 'noindex, nofollow'
  description: 'Pages are the highest order of component and are the most opinionated in nature.'
page_subtitle_before: 'Components'
page_title: 'Pages'
page_subtitle_after: 'Penn State World Campus'
menu_link_title: 'Pages'
sort_order: 7
---

{% apply markdown_to_html %}
Pages are the highest order of component and are the most opinionated in nature.

## Explore the various pages
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

