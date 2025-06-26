---
title: 'Components - Molecules - Credentials'
meta:
  robots: 'noindex, nofollow'
  description: 'Credentials stylized icon / text pairs that represent qualifications or accomplishments.'
page_subtitle_before: 'Molecules'
page_title: 'Credentials'
page_subtitle_after: 'Penn State World Campus'
menu_link_title: 'Credentials'
sort_order: 1
---
{% apply markdown_to_html %}
  Credentials stylized icon / text pairs that represent qualifications or accomplishments.
{% endapply %}

{% set variables %}
  {% apply markdown_to_html %}
    | Variable   | Type   | Required | Description                                                                                                                         |
    |------------|--------|----------|---------------------------------------------------------------------------------------------|
    | icon       | string | true     | The name of the icon to use. This should correspond to a known sprite name.                 |
    | text       | string | false    | The text to show.                                                                           |
    | icon_alt   | string | false    | An optional, visually-hidden string used to provide a text-based equivalent for the sprite. |
  {% endapply %}
{% endset %}


{% include 'partials/component-docs.twig' with {
  installation: {
    npm: {
      package: 'credential',
    },
  },
  usage: {
    twig: '
{% include "@oe/credential/credential.twig" with {
  icon: <string>,
  text: <string>,
} only %}',
  },
  variables: variables,
  examples: [
    {
      label: 'Academics', 
      content: '
{% include "@oe/credential/credential.twig" with {
  icon: "fas-building-columns",
  icon_alt: "Academic role",
  text: "Fellow (FACHE), American College of Healthcare Executives",
} only %}'
    },
    {
      label: 'Business Roles', 
      content: '
{% include "@oe/credential/credential.twig" with {
  icon: "fas-briefcase",
  icon_alt: "Business role",
  text: "C.E.O., BigCorp Inc.",
} only %}'
    },
    {
      label: 'Certificate', 
      content: '
{% include "@oe/credential/credential.twig" with {
  icon: "fas-certificate",
  icon_alt: "Credential",
  text: "Special Education Credential, Chapman University",
} only %}'
    },
    {
      label: 'Degree', 
      content: '
{% include "@oe/credential/credential.twig" with {
  icon: "fas-graduation-cap",
  icon_alt: "Degree",
  text: "Ph.D., Accounting, University of Maryland",
} only %}'
    },
    {
      label: 'Medical role', 
      content: '
{% include "@oe/credential/credential.twig" with {
  icon: "fas-briefcase-medical",
  icon_alt: "Medical role",
  text: "Emergency Medical Residency, WellSpan York Hospital",
} only %}'
    },
  ]
} only %}