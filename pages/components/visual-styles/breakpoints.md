---
title: 'Components - Breakpoints'
meta:
  robots: 'noindex, nofollow'
  description: 'Although generally discouraged, certain named breakpoints are supported.'
page_subtitle_before: 'Penn State World Campus'
page_title: 'Breakpoints'
page_subtitle_after: 'Design System Demo'
menu_link_title: 'Breakpoints'
sort_order: 0
---
{% apply markdown_to_html %}
Although every effort has been made to avoid using breakpoints within
components, sometimes it is inevitable. It is recommended that any
customizations also avoid using breakpoints, but rather using flex-based
layouts and relying on minimum widths to collapse content into columns.

When using breakpoints, always start with mobile-first.

## Named Breakpoints
{% endapply %}

{% set breakpoints = [
  { name: 'Extra extra small', variable: '$bp_xxs', width: '320px' },
  { name: 'Extra small', variable: '$bp_xs', width: '550px' },
  { name: 'Smaller', variable: '$bp_smaller', width: '675px' },
  { name: 'Small', variable: '$bp_s', width: '800px' },
  { name: 'Medium', variable: '$bp_m', width: '950px' },
  { name: 'Large', variable: '$bp_l', width: '1024px' },
  { name: 'Extra large', variable: '$bp_xl', width: '1280px' },
] %}
{% for breakpoint in breakpoints %}
  {% apply markdown_to_html %}
    ### {{ breakpoint.name }}
    | SCSS variable             | Width                  |
    | ------------------------- | ---------------------- |
    | {{ breakpoint.variable }} | {{ breakpoint.width }} |
    <div style="background:var(--sky-blue);padding:1rem;margin-bottom:2rem;width:{{ breakpoint.width }}">
      {{ breakpoint.width }} wide
    </div>
  {% endapply %}
{% endfor %}
