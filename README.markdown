Generic templates
=================

A set of introductory templates for using in [r3][r3]. They illustrate the
technique of splitting pages up into very small fragments for easier
localisation.


Naming scheme
-------------

*   Anything which is internal to the workings of [r3][r3] is prefixed with
    `r3_`.

*   Output type is indicated by the extension. So, for example:
    *   HTML pages are produced by templates with the `.html` extension.
    *   Atom feeds are produced by templates with the `.atom` extension.
    *   Any template which is internal to the workings of [r3][r3], or
        otherwise should not produce output, has the extension `.ros`.

*   Generic target templates (the base template that all others are included 
    by) are named `r3_target_OUTPUT.ros`, where OUTPUT is the output type. So,
    for example:
    *   The default HTML template is named `r3_target_html.ros`.
    *   The default Atom template is named `r3_target_atom.ros`.

*   A lightweight namespacing scheme is used in the scaffolding templates
    (those that build the main sections of a rendered document). This is done
    by prefixing the filename with the main section it is in, for example
    `head_meta_keywords.html` indicates that this is within the `head` 
    element, and is a sub-template of the `head_meta.html` template.
    
    This technique is abandoned very quickly within the `body` area of HTML
    however, as this would result in incredibly lengthy filenames. For the
    most part, prefixes are kept to one level, so for example:
    *   `body.html` includes `body_footer.html`
    *   `body_footer.html` includes `footer_legal.html`
    *   `footer_legal.html` includes `legal_copyright.html`
    
    Once the progression to actual site content is made, any attempt at
    consistent naming scheme is then abandoned and left as an exercise to the
    site authors.


[r3]:http://developer.yahoo.com/r3/
