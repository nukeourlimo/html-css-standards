# html-css-standards

##HTML

###General HTML markup rules

* Use tabs, you can set whatever spacing you like so there is no need to adopt anyone elses preferences
* Keep indentation consistant, this will help with debugging and being able to see structure
* Use HTML5 doctype
* Give html element a lang attribute (en-GB)
* Use IE compatibility mode
* Character encoding (UTF-8)
* Use as few elements as possible when possible
* Avoid adding markup directly with JS unless using a templating engine.

###Markup Standards

Please visit http://diveintohtml5.info/semantics.html#new-elements for detailed descrition of HTML5 elements.  It makes sense to use these where relevent as can prevent additional css classes, such as, "article"

####Headings

Every frontend or backend developer will almost without fail markup a page differently, however when working in a team it is important to come to a concensus on mark up standards. Headers are devisive as their implementation is very much based on context however I would suggest the following as a guide http://www.w3.org/TR/WCAG20-TECHS/H42.html

####Accessibility
These are goals ALL of our webapps and websites should strive to http://www.w3.org/TR/WCAG20/

##CSS

At present we exclusively use SCSS following an atomised approach.  This approach is still being finalised, however here are some of the key points from our current process:

###Our Atomised CSS Approach 

* Atoms - Apply to one type of item, for instance all basic styles for inputs and typography
* Molecules - These are small groups of elements, for instance a label/input pair which will be resused.
* Organisms - Groups of molecules or component styles.
* Pages - Specific overrides for organisms or molecules based on the page they are on.
* Templates - Specific overrides for organisms or molecules, these override the pages styles where necessary

For more information the following site is a good starting point http://patternlab.io/

###General CSS(SCSS) rules

* Indent everything correctly using a single tab, i like indentation to appear 4 spaces wide(but be a tab) to give clear definition when nesting
* Nest any element modifiers in the element using the & symbol in SCSS where necessary
* Media Queries should appear directly in the element
* Start with mobile first, then you may only need one or two media queries to modify the layout for larger sizes
* Use a mixin for transitions or the following format ```transition: $prop $timing $ease $delay```
