---
title: 'Components - Colors'
meta:
  robots: 'noindex, nofollow'
  description: 'The design system color palette, based on the Penn State Brand Book.'
page_subtitle_before: 'Penn State World Campus'
page_title: 'Colors'
page_subtitle_after: 'Design System Demo'
menu_link_title: 'Colors'
sort_order: 1
---
{% apply markdown_to_html %}
  The color foundation of Penn State Outreach and Online Education, based on Penn State branding guidelines.
{% endapply %}

{% set colors = {
  'Black': 'var(--black)',
  'White': 'var(--white)',
  'Light Grey': 'var(--light-grey)',
  'Light Mauve': 'var(--light-mauve)',
  'Medium Grey': 'var(--medium-grey)',
  'Slate Light': 'var(--slate-light)',
  'Limestone': 'var(--limestone)',
  'Medium Dark Grey': 'var(--medium-dark-grey)',
  'Slate': 'var(--slate)',
  'Nittany Navy': 'var(--nittany-navy)',
  'Beaver Blue': 'var(--beaver-blue)',
  'Sky Blue': 'var(--sky-blue)',
  'Pugh Blue': 'var(--pugh-blue)',
  'PA Link': 'var(--pa-link)',
  'PA Link Light': 'var(--pa-link-light)',
  'Creek': 'var(--creek)',
  'Penns Forest': 'var(--penns-forest)',
  'Keystone Light': 'var(--keystone-light)',
  'Keystone': 'var(--keystone)',
  'Invent Orange': 'var(--invent-orange)',
  'Invent Orange Light': 'var(--invent-orange-light)',
  'Error Red': 'var(--error-red)',
} %}

{% set items = [] %}
{% for name, var in colors %}
  {% set color %}
    <div style="aspect-ratio:4;background-color: {{ var }};border-radius:.5rem .5rem 0 0;"></div>
    {% apply markdown_to_html %}
      | Name | Property |
      | ---- | -------- |
      | {{ name }} | {{ var }} |
    {% endapply %}
  {% endset %}
  {% set items = items|merge([color]) %}
{% endfor %}

{% include '@psu-ooe/grid/grid.twig' with {
  items: items
} only %}