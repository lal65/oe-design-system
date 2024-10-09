---
title: 'Components - Organisms'
meta:
  robots: 'noindex, nofollow'
  description: 'Organisms are complex higher order components that may be formed by the combination of many atoms and molecules.'
page_subtitle_before: 'Components'
page_title: 'Organisms'
page_subtitle_after: 'Penn State World Campus'
menu_link_title: 'Organisms'
sort_order: 3
---

{% apply markdown_to_html %}
  Organisms in a design system are components that are made up of groups of
  molecules and/or other organisms. They are the building blocks of a user
  interface and are usually more complex than molecules but less complex
  than templates. Organisms are often reusable and can be combined with other
  organisms to create more complex user interfaces.
{% endapply %}

{% include 'partials/grid-submenu.twig' with {
  heading: {
    content: 'Explore the various organisms',
    level: 2,
  },
  path: 'components/organisms',
} only %}

