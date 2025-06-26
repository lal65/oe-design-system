# Congratulations on your new website!
Go forth with confidence in knowing that your website is secure, performant, accessible, and perfectly on-brand!

## Website Management
All content is managed through the GitHub GUI.

## Site Configuration
You will find a `config.yml` file in your repository root. This file allows you to configure various site-wide information about your website.

### Example Configuration
```yml
base_path: 'static-site-template'
site_name: 'Demo Static Site'
site_description: 'A demonstration of a simple static site.'
theme_color: '#1e407c'
tile_color: '#1e407c'
background_color: '#1e407c'
```

#### base_path
The `base_path` variable is used when your site is hosted without a CNAME record.  Your site will exist at `https://your-organization.github.io/{{ base_path }}`.  For example, `https://psu-online-education.github.io/static-site-template`.

If using a CNAME for your site, this variable can be safely deleted.

#### site_name
The `site_name` variable will be used in various metatags. It is appended to the `<title>` HTML attribute, so that the title will take the form of `{{ page_title }} | {{ site_name }}`.  For example, an "Accessibility Statement" page with a site name of "Demo Static Site" would yield a `<title>` of "Accessibility Statement | Demo Static Site".

#### site_description

#### theme_color
The `theme_color` variable will allow some browsers to style GUI elements outside of the webpage!  It is only supported under certain conditions, but can add a unique branding experience.

#### tile_color
The `tile_color` variable allows for customization of certain icons when a shortcut to your website is added to certain Microsoft Windows start screens.

#### background_color
The `background_color` variable allows for customization of the application page color before stylesheets begin loading.

## Content Management
Content is primarily managed through MarkDown files.  For more information on MarkDown, be sure to read [Basic writing and formatting syntax](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax) from the GitHub documentation.

### Pages
All pages exist within the _pages_ folder. All pages are 100% self-contained within a single file.

#### Page Structure
Pages have two basic parts: metainformation and content.

##### Page Metainformation
Metainformation is provided through a mechanism called "Front Matter".  Front Matter is essentially YAML configuration stored between two sets of `---` characters.  For example:
```md
---
title: 'Homepage'
meta:
  robots: 'index, follow'
  description: 'Welcome to the demo static site homepage.'
page_subtitle_before: 'Penn State World Campus'
page_title: 'Example Static Site'
page_subtitle_after: 'World Campus Design System'
page_image: 'demo.jpg'
---
```
###### title
The `title` variable will be used in the `<title>` HTML element.

###### meta
The `meta` object consists of a group of variables that dictate how syndicated content interacts with third parties.

###### meta: robots
The `robots` variable influences how web crawlers interact with this specific page.

###### meta: description
The `description` variable influences how web crawlers interpret this specific page.

###### page_subtitle_before
The `page_subtitle_before` variable contains text which is displayed on the page title block.

###### page_title
The `page_title` variable contains text which is displayed on the page title block.

###### page_subtitle_after
The `page_subtitle_after` variable contains text which is displayed on the page title block.

###### page_image
The `page_image` variable, if used, will cause the page title to display within an image banner block.

## Advanced
@TODO: Docs!

### Block Management
@TODO: Docs!
