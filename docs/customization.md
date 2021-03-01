---
template: overrides/main.html
---

# Customization

netSys can be customized in different ways. netSys is customized differently depending on the build.
!!! info
    netSys Developer Builds are currently the only build that is documented at the moment.

=== "netSys Embedded"

    !!! fail
        netSys Embedded Documentation is being worked on.

=== "netSys Developer Build"

 
 

    Customization is an important part of netSys.


    ## Adding assets


    !!! warning "Theme extension prerequisites"

    As the `custom_dir` variable is used for the theme extension process,
    Material for MkDocs needs to be installed via `pip` and referenced with the
    `name` parameter in `mkdocs.yml`. It will not work when cloning from `git`.


    ``` sh
    .
    ├─ .icons/                             # Bundled icon sets
    ├─ assets/
    │  ├─ images/                          # Images and icons
    │  ├─ javascripts/                     # JavaScript
    │  └─ stylesheets/                     # Stylesheets
    ├─ partials/
    │  ├─ integrations/                    # Third-party integrations
    │  │  ├─ analytics.html                # - Google Analytics
    │  │  └─ disqus.html                   # - Disqus
    │  ├─ languages/                       # Localized languages
    │  ├─ footer.html                      # Footer bar
    │  ├─ header.html                      # Header bar
    │  ├─ language.html                    # Localized labels
    │  ├─ logo.html                        # Logo in header and sidebar
    │  ├─ nav.html                         # Main navigation
    │  ├─ nav-item.html                    # Main navigation item
    │  ├─ palette.html                     # Color palette
    │  ├─ search.html                      # Search box
    │  ├─ social.html                      # Social links
    │  ├─ source.html                      # Repository information
    │  ├─ source-date.html                 # Last updated date
    │  ├─ source-link.html                 # Link to source file
    │  ├─ tabs.html                        # Tabs navigation
    │  ├─ tabs-item.html                   # Tabs navigation item
    │  ├─ toc.html                         # Table of contents
    │  └─ toc-item.html                    # Table of contents item
    ├─ 404.html                            # 404 error page
    ├─ base.html                           # Base template
    └─ main.html                           # Default page
    ```

    ### Overriding partials

    In order to override a partial, we can replace it with a file of the same name
    and location in the `overrides` directory. For example, to replace the original
    `footer.html`, create a `footer.html` file in the `overrides/partials`
    directory:

    ``` sh
    .
    ├─ overrides/
    │  └─ partials/
    │     └─ footer.html
    └─ mkdocs.yml
    ```

    MkDocs will now use the new partial when rendering the theme. This can be done
    with any file.

    ### Overriding blocks

    Besides overriding partials, it's also possible to override (and extend)
    _template blocks_, which are defined inside the templates and wrap specific
    features. To override a block, create a `main.html` file inside the `overrides`
    directory:

    Material for MkDocs provides the following template blocks:

    | Block name   | Wrapped contents                                |
    | ------------ | ----------------------------------------------- |
    | `analytics`  | Wraps the Google Analytics integration          |
    | `announce`   | Wraps the announcement bar                      |
    | `config`     | Wraps the JavaScript application config         |
    | `content`    | Wraps the main content                          |
    | `disqus`     | Wraps the Disqus integration                    |
    | `extrahead`  | Empty block to add custom meta tags             |
    | `fonts`      | Wraps the font definitions                      |
    | `footer`     | Wraps the footer with navigation and copyright  |
    | `header`     | Wraps the fixed header bar                      |
    | `hero`       | Wraps the hero teaser (if available)            |
    | `htmltitle`  | Wraps the `<title>` tag                         |
    | `libs`       | Wraps the JavaScript libraries (header)         |
    | `scripts`    | Wraps the JavaScript application (footer)       |
    | `source`     | Wraps the linked source files                   |
    | `site_meta`  | Wraps the meta tags in the document head        |
    | `site_nav`   | Wraps the site navigation and table of contents |
    | `styles`     | Wraps the stylesheets (also extra sources)      |
    | `tabs`       | Wraps the tabs navigation (if available)        |


    !!! warning "Automatically generated files"

        Never make any changes in the `material` directory, as the contents of this
        directory are automatically generated from the `src` directory and will be
        overridden when the theme is built.

