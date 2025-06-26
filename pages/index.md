---
title: 'Homepage'
meta:
  robots: 'noindex, nofollow'
  description: 'Penn State World Campus Design System Handbook.'
page_subtitle_before: 'Penn State World Campus'
page_title: 'Design System'
page_subtitle_after: 'Documentation & Handbook'
page_image: 'index.jpg'
menu_link_title: 'Home'
sort_order: 0
---
<br><br>
{% apply markdown_to_html %}
  ## Introducing the Penn State World Campus Design System.
  The World Campus Design System is a cutting-edge platform that is dedicated
  to producing top-of-the-line digital experiences. With a focus on
  accessibility, security, performance, and the Penn State brand, this 
  platform ensures that every website created with it is of the highest
  quality.
{% endapply %}

{% set accessibility %}
  {% apply markdown_to_html %}
    ### Accessible <span class="text--contrasting">by Default</span>
    Accessibility is ***the*** top priority for the World Campus design. By
    adhering to accessibility standards and guidelines, websites built with
    this platform are inclusive and can be easily accessed by all users,
    regardless of their abilities.
  {% endapply %}
  {% include '@oe/read-more/read-more.twig' with {
    url: '/' ~ (base_path ? base_path ~ '/') ~ 'accessibility',
    title: 'Discover how we make Penn State more accessible'
  } only %}
{% endset %}

{% set security %}
  {% apply markdown_to_html %}
    ### Security <span class="text--contrasting">Without Compromise</span>
    One of the key benefits of using the World Campus design system is its
    emphasis on security. By following best practices, websites created with
    this platform are protected against potential threats and data breaches.
  {% endapply %}
  {% include '@oe/read-more/read-more.twig' with {
    url: '/' ~ (base_path ? base_path ~ '/') ~ 'security',
    title: 'Explore our security mechanisms'
  } only %}
{% endset %}

{% set performance %}
  {% apply markdown_to_html %}
    ### Optimized <span class="text--contrasting">for Speed</span>
    Performance is a key aspect of the World Campus design system. By
    optimizing for speed and efficiency, end-users enjoy lightning fast, 
    low-carbon digital experiences. Tested against Web Vital metrics, site
    owners reap the SEO benefits.
  {% endapply %}
  {% include '@oe/read-more/read-more.twig' with {
    url: '/' ~ (base_path ? base_path ~ '/') ~ 'performance',
    title: 'Recognize what ethical web design looks like'
  } only %}
{% endset %}

{% set brand %}
  {% apply markdown_to_html %}
    ### On Brand. <span class="text--contrasting">Always.</span>
    The World Campus design system helps to maintain a consistent and
    professional design across all digital experiences that aligns with the
    Penn State brand identity.
  {% endapply %}
  {% include '@oe/read-more/read-more.twig' with {
    url: '/' ~ (base_path ? base_path ~ '/') ~ 'brand',
    title: 'Learn how we align with the Penn State brand'
  } only %}
{% endset %}
<br>
{% include '@oe/icon-list/icon-list.twig' with {
  columns: 2,
  items: [
    { content: accessibility, icon: 'fas-child-reaching' },
    { content: security, icon: 'fas-lightbulb-on' },
    { content: performance, icon: 'fas-bolt' },
    { content: brand, icon: 'fas-list-check' },
  ],
} only %}