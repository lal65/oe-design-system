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
{% endapply %}

{% include 'partials/grid-submenu.twig' with {
  heading: {
    content: 'Explore the various atoms',
    level: 2,
  },
  path: 'components/atoms',
} only %}
