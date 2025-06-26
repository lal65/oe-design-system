---
title: 'Homepage'
meta:
  robots: 'noindex, nofollow'
  description: 'Welcome to the demo static site homepage.'
page_subtitle_before: 'Design System'
page_title: 'Accessibility'
page_subtitle_after: 'Penn State World Campus'
page_image: 'accessibility.jpg'
menu_link_title: 'Accessibility'
sort_order: 1
---
{% apply markdown_to_html %}

  The Penn State World Campus design system was developed from the ground-up
  with accessibility in mind, ensuring that all users, regardless of ability,
  can easily navigate and interact with the website.
  
  ## Accessibility Baked In - Not Bolted On
  The design system incorporates the Web Content Accessibility Guidelines AA
  success criteria, which helps to ensure that users with visual, auditory, 
  motor, or cognitive disabilities can access and engage with the online
  content effectively.  Several aspects of the design system are compliant
  with various AAA criteria, wherever possible while still meeting sometimes
  competing branding needs.
  
  ## Labelling and Navigation
  One way in which the World Campus design system meets WCAG AA standards is
  through its use of clear and consistent navigation. The system emphasizes
  the use of descriptive labels for links and buttons, making it easier for
  users using screen readers or other assistive technologies to understand the
  purpose of each element. Additionally, the system includes skip navigation
  links that allow users to bypass repetitive content and go directly to the
  main content of the page, improving efficiency for all users.
  
  ## Effective Color Schemes
  Another way in which the World Campus design system meets WCAG AA criteria is
  through its use of color contrast. The system ensures that text and
  interactive elements have sufficient contrast with background colors, making
  it easier for users with visual impairments to read and interact with the
  content. By following the recommended color contrast ratios outlined in the
  WCAG AA guidelines, the World Campus design system provides a more inclusive
  experience for all users. This includes highly curated custom focus indicator
  styles.
  
  ### Automatic Color Contrasting
  The most advanced feature in this regard is the use of automatic color
  contrasting baked into many components. This allows components to respond to
  the client-side context that they find themselves in and automatically choose
  an appropriate color profile. For example, if text exists in a container that
  is dark, the text takes on a light color. This functionality even works
  **_without javascript enabled_**, making it a very Marketer-friendly platform
  for running A/B testing, etc.

  ## Setting The Bar High
  In conclusion, the Penn State World Campus design system demonstrates a
  strong commitment to accessibility by incorporating WCAG2.1 AA standards
  into its design and development process. By focusing on clear navigation,
  color contrast, and alternative text for images, the system provides an
  inclusive online experience for all users, regardless of their abilities.
  Through its dedication to accessibility, the World Campus design system
  sets a high standard for other offerings to follow in creating a more
  accessible web for everyone.

{% endapply %}