---
title: 'Components - Atoms - Forms'
meta:
  robots: 'noindex, nofollow'
  description: 'Forms are elements containing interactive controls for submitting information.'
page_subtitle_before: 'Penn State World Campus'
page_title: 'Forms'
page_subtitle_after: 'Design System Demo'
menu_link_title: 'Forms'
sort_order: 0
---
{% apply markdown_to_html %}
  Forms are elements containing interactive controls for submitting information.
{% endapply %}

{% include 'partials/component-docs.twig' with {
  installation: {
    npm: {
      package: 'form',
    },
  },
  usage: {
    html: '<form>
  <label for="demo_form_input">Demo input</label>
  <input name="demo_form_input" id="demo_form_input">
  <button>Submit</button>
</form>',
  }
} only %}

<br>
<br>
{% apply markdown_to_html %}
  ## Examples
{% endapply %}

<form>
  <label for="demo_form_input">Demo input</label>
  <input name="demo_form_input" id="demo_form_input">
  <button>Submit</button>
</form>
<br>
<br>

{% set example_on_dark %}
<form>
  <label for="demo_form_input">Demo input</label>
  <input name="demo_form_input" id="demo_form_input">
  <button>Submit</button>
</form>
{% endset %}
{% include '@psu-ooe/callout/callout.twig' with {
  background: 'blue-gradient',
  content: example_on_dark,
} only %}