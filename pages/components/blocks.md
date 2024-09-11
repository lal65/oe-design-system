---
title: 'Components - Blocks'
meta:
  robots: 'noindex, nofollow'
  description: 'Blocks are complete, opinionated design concepts offer turn-key functionality and are expected to be added directly to layouts, regions, and pages. Some examples include page titles, and special use menus.'
page_subtitle_before: 'Components'
page_title: 'Blocks'
page_subtitle_after: 'Penn State World Campus'
menu_link_title: 'Blocks'
sort_order: 4
---

{% apply markdown_to_html %}
  Blocks are complete, opinionated design concepts offer turn-key functionality
  and are expected to be added directly to layouts, regions, and pages. Some
  examples include page titles, and special use menus.

  ## Explore the various blocks
{% endapply %}

{% set grid_items = [] %}
{% for item in get_menu_items()['components']['below']['components/blocks']['below'] %}
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
