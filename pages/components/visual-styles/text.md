---
title: 'Components - Text'
meta:
  robots: 'index, follow'
  description: 'Explore the components that are available for use in the design system.'
page_subtitle_before: 'Penn State World Campus'
page_title: 'Text'
page_subtitle_after: 'Design System Demo'
menu_link_title: 'Text'
sort_order: 3
---
{% apply markdown_to_html %}
  A wide variety of text styles are supported, each of which have been
  carefully crafted to have accessible contrast in both light and dark
  contexts.
{% endapply %}
{% apply markdown_to_html %}
  ## Default text
  By default, text inherits the all the default design system typography
  settings. This behavior can be used to revert an element back to the default.
  For example, links are normally `pa-link`, but can be reverted to `white` by
  applying a text class inside of it.
{% endapply %}

{% apply markdown_to_html %}
  ### Default text example
{% endapply %}
{{ example('<span class="text">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</span>', ['light', 'dark'])|raw }}
<br>

{% apply markdown_to_html %}
  ## Text weight modifiers
  There are two supported text weight modifiers that can be used to make the
  default weight heavier.
{% endapply %}

{% for weight in ['semibold', 'bold'] %}
{% apply markdown_to_html %}
### {{ weight|capitalize }}
{% endapply %}
{{ example('<span class="text text--weight-' ~ weight ~ '">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</span>', ['light', 'dark'])|raw }}
<br>
{% endfor %}

{% apply markdown_to_html %}
  ## Text size modifiers
  There are 15 supported text size modifiers. Certain modifiers may have
  varying actual sizes based on viewport and/or container dimensions.
{% endapply %}
{% for size in ['4xsmall', '3xsmall', '2xsmall', 'xsmall', 'small', 'msmall', 'medium', 'mlarge', 'large', 'xlarge', '2xlarge', '3xlarge', '4xlarge', '5xlarge', '6xlarge'] %}
  {% apply markdown_to_html %}
  ### {{ size|capitalize }}
  {% endapply %}
  {{ example('<span class="text text--size-' ~ size ~ '">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</span>', ['light', 'dark'])|raw }}
  <br>
{% endfor %}