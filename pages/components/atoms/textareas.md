---
title: 'Components - Atoms - Textareas'
meta:
  robots: 'noindex, nofollow'
  description: 'Textareas are a common form control for entering generic multiple lines of text.'
page_subtitle_before: 'Atoms'
page_title: 'Textareas'
page_subtitle_after: 'Penn State World Campus'
menu_link_title: 'Textareas'
sort_order: 0
---
{% apply markdown_to_html %}
  Textareas are a common form control for entering generic multiple lines of text.
{% endapply %}

{% include 'partials/component-docs.twig' with {
  installation: {
    npm: {
      package: 'textarea',
    },
  },
  usage: {
    html: '<textarea></textarea>',
  }
} only %}
<br>
<br>
{% include 'partials/textarea-examples.twig' with {
  type: 'text',
  variations: [
    ['disabled'],
  ],
} only %}