---
title: 'Security'
meta:
  robots: 'noindex, nofollow'
  description: 'Security is important..'
page_subtitle_before: 'Design System'
page_title: 'Security'
page_subtitle_after: 'Penn State World Campus'
page_image: 'security.jpg'
menu_link_title: 'Security'
sort_order: 2
---
{% apply markdown_to_html %}

  ## Keeping It Simple
  One of the core principals of the design system is that as much functionality
  as possible hinges on a no-tech approach to security. At the most basic level
  the design system can easily be used within static websites. Having little to
  no attack surface, these "set it and forget it" kind of websites are perfect
  for hosting information that rarely changes.

  ## Secure By Default
  Although the design system does not take an opinionated stance on the
  templating layer, the Twig language provides automatic content escaping
  mechanisms that greatly reduces the chance of cross site scripting
  vulnerabilities. Consumers are free to disable the protections afforded
  by this, but the templating layer takes a "Secure By Default" posture. The
  primary CMS integration, Drupal, also takes this posture.

  ## Trust No One
  There are various javascript dependent components and utilities that are
  provided, and each are carefully curated to avoid the potential for
  reflected XSS as well. This includes never trusting arbitrary client-side
  markup in the rare cases where markup manipulation is required. As such,
  calls to set `innerHTML` and other such dangerous methods are avoided.

{% endapply %}