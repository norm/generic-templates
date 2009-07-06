Generic templates
=================

A set of introductory templates for using in r3. They illustrate the technique
of splitting pages up into very small fragments for easier localisation.


Naming scheme
-------------

* Anything which is internal to the workings of r3 is prefixed with 'r3_'.

* Output type is indicated by the extension. So, for example:

  * HTML pages are produced by templates with the '.html' extension.
  * Atom feeds are produced by templates with the '.atom' extension.
  * Any template which is internal to the workings of r3, or otherwise 
    should not produce output, has the extension '.ros'.

* Generic target templates (the base template that all others are included 
  by) are named 'r3_target_OUTPUT.ros', where OUTPUT is the output type. So,
  for example:
  
  * The default HTML template is named 'r3_target_html.ros'.
  * The default Atom template is named 'r3_target_atom.ros'.
