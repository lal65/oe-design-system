---
title: 'Components - Atoms'
meta:
  robots: 'noindex, nofollow'
  description: 'Atoms form the smallest reusable units of a design. They may include features like headings, buttons, and other low level components.'
page_subtitle_before: 'Components'
page_title: 'Atoms'
page_subtitle_after: 'Penn State World Campus'
menu_link_title: 'Atoms'
sort_order: 1
---

{% apply markdown_to_html %}
  In a design system, atoms represent the most basic and elemental building
  blocks of design elements. They are the smallest units of design that cannot
  be broken down any further without losing their essential identity. Atoms
  include things like headings, buttons, icons, and form elements. They serve
  as the foundation for building more complex design components and patterns
  within a system.
  ## Explore the various atoms
{% endapply %}

{% set grid_items = [] %}
{% for item in get_menu_items()['components']['below']['components/atoms']['below'] %}
  {% set grid_item %}
    {% include '@psu-ooe/navigation-tile/navigation-tile.twig' with {
      link: { url: item['url'], label: item['title'] },
      description: item['description'],
    } only %}
  {% endset %}
  {% set grid_items = grid_items|merge([grid_item]) %}
{% endfor %}

{% include '@psu-ooe/grid/grid.twig' with {
  items: grid_items
} only %}