---
title: 'Components - Molecules - Background containers'
meta:
  robots: 'noindex, nofollow'
  description: 'Background containers are special containers that provide strategically positioned ambient sprites.'
page_subtitle_before: 'Molecules'
page_title: 'Background containers'
page_subtitle_after: 'Penn State World Campus'
menu_link_title: 'Background containers'
sort_order: 1
---
{% apply markdown_to_html %}
  Background containers are special containers that provide strategically
  positioned ambient sprites.  There are several modifiers that allow for a
  more highly controlled positioning of said sprites in relationship with the
  content that is expected to be placed inside the container.
{% endapply %}

{% set variables %}
  {% apply markdown_to_html %}
    | Variable         | Type   | Required | Description                                       |
    |------------------|--------|----------|---------------------------------------------------|
    | content          | string | true     | The content to render inside the container.       |
    | color            | string | true     | Must match a documented color modifier.           |
    | background_image | string | false    | May match a documented background image modifier. |
    | padding          | string | false    | May match a documented padding modifier.          |
    | width            | string | false    | May match a documented width modifier.            |
  {% endapply %}
{% endset %}

{% set modifiers %}
  {% apply markdown_to_html %}

    ### Colors

    | Color        | Description                        |
    |--------------|------------------------------------|
    | light-grey   | Displays a light-grey background   |
    | beaver-blue  | Displays a beaver-blue background  |

    ### Background images

    | Image                      | Description                                                                                 |
    |----------------------------|---------------------------------------------------------------------------------------------|
    | hub-geometric:topleft      | Hub geometric positioned to the left top corner of the container.                           |
    | hub-geometric:topright     | Hub geometric positioned to the right top corner of the container.                          |
    | hub-geometric:bottomleft   | Hub geometric positioned to the left bottom corner of the container.                        |
    | hub-geometric:bottomright  | Hub geometric positioned to the right bottom corner of the container.                       |
    | shield:left                | Community shield positioned to the left side of the container.                              |
    | shield:right               | Community shield positioned to the right side of the container.                             |
    | shield:bottomright         | Community shield positioned to the right-bottom corner of the container                     |
    | shield:topleft-bottomright | Dual community shields positioned to the top-left and bottom-right corners of the container |

    ### Paddings

    | Padding | Description                                               |
    |---------|-----------------------------------------------------------|
    | small   | Adds a small amount of vertical padding to the container. |
    | large   | Adds a large amount of vertical padding to the container. |

    ### Widths

    | Width  | Description                                                                  |
    |--------|------------------------------------------------------------------------------|
    | narrow | Causes a shift in the background sprite to better accommodate narrow spaces. |

 {% endapply %}
{% endset %}

{% set examples = [] %}
{% for background in ['hub-geometric:topleft', 'hub-geometric:topright', 'hub-geometric:bottomleft', 'hub-geometric:bottomright', 'shield:left', 'shield:right', 'shield:bottomright', 'shield:topleft-bottomright'] %}
  {% for color in ['light-grey', 'beaver-blue'] %}
    {% for width, width_label in {'': 'Normal width', 'narrow': 'Narrow width'} %}
      {% set examples = examples|merge([{
        unwrapped: true,
        label: background ~ ' (' ~ color ~ ',' ~ width_label ~ ')',
        content: '
{% include "@oe/background-container/background-container.twig" with {
  color: "' ~ color ~ '",
  width: "' ~ width ~ '",
  background_image: "' ~ background ~ '",
  content: "
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            ",
} only %}',
    }]) %}
    {% endfor %}
  {% endfor %}
{% endfor %}

{% include 'partials/component-docs.twig' with {
  installation: {
    npm: {
      package: 'background-container',
    },
  },
  usage: {
    twig: '
{% include "@oe/background-container/background-container.twig" with {
  color: <color>,
  background_image: <image>,
  content: <content>
} only %}',
  },
  variables: variables,
  modifiers: modifiers,
  examples: examples,
} only %}