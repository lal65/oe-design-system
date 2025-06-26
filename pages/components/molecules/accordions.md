---
title: 'Components - Molecules - Accordions'
meta:
  robots: 'noindex, nofollow'
  description: 'Accordions are disclosure elements in which information is visible when open.'
page_subtitle_before: 'Molecules'
page_title: 'Accordions'
page_subtitle_after: 'Penn State World Campus'
menu_link_title: 'Accordions'
sort_order: 1
---
{% apply markdown_to_html %}
  Accordions are disclosure elements in which information is visible when open.
  While similar to details elements, accordions offer more flexibility with
  semantic aspects and animations.
{% endapply %}

{% set variables %}
  {% apply markdown_to_html %}
  | Variable           | Type    | Required | Description                                                                                                                        |
  |--------------------|---------|----------|------------------------------------------------------------------------------------------------------------------------------------|
  | toggle_content     | string  | true     | The content to render within the accordion toggle element.                                                                         |
  | expandable_content | string  | true     | The content to render within the accordion expandable element.                                                                     |
  | toc_label          | string  | false    | An optional label for this component if it were to appear in a table of contents menu.                                             |
  | heading_level      | integer | false    | An integer, between 1 and 6 that denotes the heading level. If provided, the accordion toggle will have heading semantics applied. |
  | heading_style      | string  | false    | If set, will override the heading style of the accordion toggle.                                                                   |
  | expanded           | boolean | false    | If set, the accordion will be expanded by default.                                                                                 |
  | indent_content     | boolean | false    | If set, the expandable content will be indented.                                                                                   |
  | label_underline    | boolean | false    | If set, the accordion label will be underlined.                                                                                    |
  | borderless         | boolean | false    | If set, the accordion will render without borders.                                                                                 |
  {% endapply %}
{% endset %}

{% set modifiers %}
  {% apply markdown_to_html %}
    ### Heading styles
    | Heading style | Description                         |
    |---------------|-------------------------------------|
    | xlarge        | This style looks like an &lt;h1&gt; |
    | large         | This style looks like an &lt;h2&gt; |
    | medium        | This style looks like an &lt;h3&gt; |
    | small         | This style looks like an &lt;h4&gt; |
    | xsmall        | This style looks like an &lt;h5&gt; |
    | 2xsmall       | This style looks like an &lt;h6&gt; |
  {% endapply %}
{% endset %}

{% include 'partials/component-docs.twig' with {
  installation: {
    npm: {
      package: 'accordion',
    },
  },
  usage: {
    twig: '
{% include "@oe/accordion/accordion.twig" with {
  id: "accordion-default",
  label: "Accordion label",
  expandable_content: "This is the accordion content."
} only %}',
  },
  variables: variables,
  modifiers: modifiers,
  examples: [
    {
      label: 'Simple usage', 
      content: '
{% include "@oe/accordion/accordion.twig" with {
  id: "simple-usage",
  label: "Default",
  expandable_content: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.",
} only %}'
    },
    {
      label: 'Borderless',
      content: '
{% include "@oe/accordion/accordion.twig" with {
  id: "borderless",
  label: "Borderless",
  expandable_content: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.",
  borderless: true,
} only %}'
    },
    {
      label: 'Heading semantics', 
      content: '
{% include "@oe/accordion/accordion.twig" with {
  id: "heading-semantics",
  label: "Heading semantics",
  expandable_content: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.",
  heading_level: 2
} only %}'
    },
    {
      label: 'Content indented', 
      content: '
{% include "@oe/accordion/accordion.twig" with {
  id: "content-indented",
  label: "Content indented",
  expandable_content: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.",
  indent_content: true,
} only %}'
    },
    {
      label: 'Underline label', 
      content: '
{% include "@oe/accordion/accordion.twig" with {
  id: "underline-label",
  label: "Underline label",
  expandable_content: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.",
  label_underline: true,
} only %}'
    },
    {
      label: 'Adjacency', 
      content: '
{% include "@oe/accordion/accordion.twig" with {
  id: "adjacent-1",
  label: "Adjacent 1",
  expandable_content: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.",
} only %}
{% include "@oe/accordion/accordion.twig" with {
  id: "adjacent-2",
  label: "Adjacent 2",
  expandable_content: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.",
} only %}
{% include "@oe/accordion/accordion.twig" with {
  id: "adjacent-3",
  label: "Adjacent 3",
  expandable_content: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.",
} only %}'
    },
  ],
} only %}