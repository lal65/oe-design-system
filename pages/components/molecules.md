---
title: 'Components - Molecules'
meta:
  robots: 'noindex, nofollow'
  description: 'Molecules are made up of various atoms working together. They may include button groups, various containers, and other elements that typically do not exist on their own.'
page_subtitle_before: 'Components'
page_title: 'Molecules'
page_subtitle_after: 'Penn State World Campus'
menu_link_title: 'Molecules'
sort_order: 2
---

{% apply markdown_to_html %}
  In a design system, molecules are the building blocks of a user interface.
  They are small, reusable components that can be combined and arranged to
  create more complex components or UI elements. Examples of molecules include
  buttons, input fields, cards, and checkboxes. By designing and documenting
  molecules within a design system, designers and developers can ensure
  consistency and efficiency across different parts of a product.

  ## Explore the various molecules
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
