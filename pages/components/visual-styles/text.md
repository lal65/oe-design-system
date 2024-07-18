---
title: 'Components - Text'
meta:
  robots: 'index, follow'
  description: 'Learn more about the various typographical utilities.'
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

{% set text_weight_modifiers_intro %}
  {% apply markdown_to_html %}
    ## Text weight modifiers
    There are two supported text weight modifiers that can be used to make the
    default weight heavier.
  {% endapply %}
{% endset %}

{% set text_weight_modifiers_examples %}
  {% for weight in ['semibold', 'bold'] %}
    {% apply markdown_to_html %}
    ### {{ weight|capitalize }}
    {% endapply %}
    {{ example('<span class="text text--weight-' ~ weight ~ '">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</span>', ['light', 'dark'])|raw }}
    {% if not loop.last %}<br>{% endif %}
  {% endfor %}
{% endset %}

{% include '@psu-ooe/expandable-section/expandable-section.twig' with {
  intro: text_weight_modifiers_intro,
  expand_label: 'Show weight modifiers',
  collapse_label: 'Close section',
  content: text_weight_modifiers_examples,
} only %}
<br>

{% set text_density_modifiers_intro %}
  {% apply markdown_to_html %}
    ## Text density modifiers
    There are 6 text density modifiers. These modifiers are typically only used
    in very specific scenarios where specialized custom typography configurations
    are applied.
  {% endapply %}
{% endset %}

{% set text_density_modifiers_examples %}
  {% for density in ['msnug', 'snug', 'xsnug', '2xsnug', '3xsnug', 'nospace'] %}
    {% apply markdown_to_html %}
      ### {{ density|capitalize }}
    {% endapply %}
    {% if density == 'nospace' %}
      {% include '@psu-ooe/alert/alert.twig' with {
      severity: 'warning',
      content: 'Use caution in where the nospace modifier is used. Some users may have difficulty reading the content!',
      } only %}
      <br>
    {% endif %}
    {{ example('<span class="text text--height-' ~ density ~ '">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</span>', ['light', 'dark'])|raw }}
    {% if not loop.last %}<br>{% endif %}
  {% endfor %}
{% endset %}

{% include '@psu-ooe/expandable-section/expandable-section.twig' with {
  intro: text_density_modifiers_intro,
  expand_label: 'Show density modifiers',
  collapse_label: 'Close section',
  content: text_density_modifiers_examples,
} only %}
<br>

{% set text_size_modifiers_intro %}
  {% apply markdown_to_html %}
    ## Text size modifiers
    There are 15 supported text size modifiers. Certain modifiers may have
    varying actual sizes based on viewport and/or container dimensions.
  {% endapply %}
{% endset %}
{% set text_size_modifiers_examples %}
  {% for size in ['4xsmall', '3xsmall', '2xsmall', 'xsmall', 'small', 'msmall', 'medium', 'mlarge', 'large', 'xlarge', '2xlarge', '3xlarge', '4xlarge', '5xlarge', '6xlarge'] %}
    {% apply markdown_to_html %}
      ### {{ size|capitalize }}
    {% endapply %}
    {{ example('<span class="text text--size-' ~ size ~ '">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</span>', ['light', 'dark'])|raw }}
    <br>
  {% endfor %}
{% endset %}

{% include '@psu-ooe/expandable-section/expandable-section.twig' with {
  intro: text_size_modifiers_intro,
  expand_label: 'Show size modifiers',
  collapse_label: 'Close section',
  content: text_size_modifiers_examples,
} only %}
<br>

{% set advanced_modifiers_intro %}
  {% apply markdown_to_html %}
    ## Advanced
    There are a few advanced / niche use cases for text utilities, but should
    only be used with caution.
  {% endapply %}
{% endset %}

{% set advanced_modifiers_examples %}
  {% apply markdown_to_html %}
    ### Forced color override: slate
    The slate color can be used for text, however it is not auto-contrast
    friendly.
  {% endapply %}
  
  {{ example('<span class="text text--color-slate">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</span>', ['light', 'dark'])|raw }}
  <br>
  {% apply markdown_to_html %}
    ### Forced color override: reversed
    The reversed color can be used for text, however it is not auto-contrast
    friendly. This variant will eventually become deprecated.
  {% endapply %}
  {{ example('<span class="text text--color-reversed">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</span>', ['light', 'dark'])|raw }}
  <br>
  
  {% apply markdown_to_html %}
    ### Forced color override: contrasting
    The contrasting text mode is used to make certain text stand out in proximity
    to text around it, however it is not auto-contrast friendly.
  {% endapply %}
  {{ example('<span class="text text--contrasting">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</span>', ['light', 'dark'])|raw }}
{% endset %}

{% include '@psu-ooe/expandable-section/expandable-section.twig' with {
  intro: advanced_modifiers_intro,
  expand_label: 'Show advanced modifiers',
  collapse_label: 'Close section',
  content: advanced_modifiers_examples,
} only %}