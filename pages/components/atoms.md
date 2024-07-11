---
title: 'Components - Atoms'
meta:
  robots: 'index, follow'
  description: 'Explore the components that are available for use in the design system.'
page_subtitle_before: 'Components'
page_title: 'Atoms'
page_subtitle_after: 'Penn State World Campus'
menu_link_title: 'Atoms'
sort_order: 1
---

{% apply markdown_to_html %}
  In a design system, atoms represent the most basic and elemental building blocks of design elements. They are the smallest units of design that cannot be broken down any further without losing their essential identity. Atoms include things like typography, colors, buttons, icons, and form fields. They serve as the foundation for building more complex design components and patterns within a system. By defining atoms in a design system, designers can establish consistency and cohesion across all elements of a product or brand.
  ## Explore the various atoms
{% endapply %}

{% set grid_items = [] %}
{% for item in get_menu_items()['components']['below']['components/atoms']['below'] %}
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