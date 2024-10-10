---
title: 'Components - Atoms - File Inputs'
meta:
  robots: 'noindex, nofollow'
  description: 'File inputs are a common form control for uploading one or more files.'
page_subtitle_before: 'Penn State World Campus'
page_title: 'File Inputs'
page_subtitle_after: 'Design System Demo'
menu_link_title: 'File Inputs'
sort_order: 0
---
{% apply markdown_to_html %}
File inputs are a common form control for uploading one or more files.
{% endapply %}

{% include 'partials/component-docs.twig' with {
  installation: {
    npm: {
      package: 'input-file',
    },
  },
  usage: {
    html: '<input type="file">',
  }
} only %}
<br>
<br>
{% include 'partials/input-examples.twig' with {
  type: 'file',
  variations: [
    ['multiple'],
    ['disabled'],
    ['multiple', 'disabled'],
  ],
} only %}