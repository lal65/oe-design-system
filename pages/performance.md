---
title: 'Performance'
meta:
  robots: 'noindex, nofollow'
  description: 'Welcome to the demo static site homepage.'
page_subtitle_before: 'Design System'
page_title: 'Performance'
page_subtitle_after: 'Penn State World Campus'
menu_link_title: 'Performance'
sort_order: 3
---
{% apply markdown_to_html %}

  Performance is one of the primary considerations for every component within
  the design system.

  ## Quantifying Performance
  Performance can mean a lot of different things. We quantify performance in a
  number of ways including enforcing dependency management, measuring asset
  size, and ultimately relying on the Core Web Vitals as set forth by Google.

  ### Loose Coupling and Dependency Management
  Through consistent use of dependency management (NPM) we are able to provide
  the correct tools to ensure that the minimal number of asset libraries are
  delevered on a per-page basis. In other words, you never have to pay for what
  you don't use.

  The only globally required component is the `base` component, which weighs a
  mere 2.5KB.

  ### Optimized Asset Delivery
  Each component provides optimized artifacts out of the box.

  ### Meeting Core Web Vitals
  The CWV assessment forms a very solid foundation for measuring website
  performance. The most impactful way that we have optimized for CWV has been
  to ensure that no components are dependent on Javascript to display properly
  on first paint. This means that no components will ever experience a Flash of
  Original Content (FoOc) or Flash of Unstyled Content (FoUC). This also means
  that all layout decisions are handled by the CSS layer.

  #### Unavoidable Performance Issues
  Due to institutional policy and licensing restrictions, we are forced to use
  Adobe hosted webfonts. These webfonts are known to cause severe performance
  problems when trying to optimize for CWV.

{% endapply %}