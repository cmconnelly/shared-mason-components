# shared-mason-components

A set of [HTML::Mason](http://www.masonhq.com/htmlmason) Perl
components that can be used to build a website.  They were
originally developed for use on my personal blog, and later
adapted for use on the [Harvey Mudd College Department of Mathematics website](https://www.math.hmc.edu/).

Many of these components were originally written to provide
similar functionality to macros in [Userland Frontier](http://scripting.com/frontier/beginning/whatFrontierIs.html) before
it became a commercial product.

Most components rely on data files in YAML format.

Most continuing development has taken place as part of maintaining
and improving the math department website, and we have added
components for handling course links, pulling out course
description information, and so on.  Further development of the 
HMC-related components is unlikely, as I have left their employ.

Note that some of these components are being modified to make them
behave better in an HTML5 world.


## Available Components


* `DTD` Generates a DTD header.  Can produce different headers
  based on arguments (e.g., HTML4, XHTML, HTML5).

* `breadcrumbs` Create a "breadcrumb trail" from the site's root
  to the current page.

* `captioned` Create an image with a caption.

* `cdlink` Create links to a course description.

* `coursedescription` Extract information from a course
  description (e.g., title, credits, prerequisites, description).

* `gr` Creates links from a dictionary of links with short
  names, link text, URL, and `alt` text (for, e.g., defining acronyms
  or abbreviations).  Glossary entries can be reused anywhere on
  the site; change the glossary file and the links will update on
  the next publish.  You can also override the defined link text
  and alt text for each individual usage.


* `hmclogo` Generates an image link to the site's home page.

* `img` Similar to `gr`, `img` allows you to insert an `<img>`
  tag with predefined alternative text.  You can override that
  text as well as change various other parameters (e.g., sizes and
  CSS classes).

* `localstyle` Allows you to define a `<%method
  localstyle>...</%method>` section in any page that will be used
  to insert page-specific CSS code.  Useful for overriding site
  settings for a single page or subsection of a site (if defined
  in an `autohandler` file).


* `navnavnav` Builds navigation menus based on the contents of
  `navigation` files in the current and enclosing directories.

* `rssfeed` Takes an RSS URL and turns it into HTML.

* `steps` Allows you to create a series of pages that can be
  stepped through consecutively (forwards or backwards).

* `stylesheet` Creates a `<link rel=` tag for a given CSS
  stylesheet name.  Handles relative links.

* `uparrowp` Creates a "return to top" link.

* `validhtml` Adds a valid HTML link based on the DTD.  (Does
  *not* check for validity; that's up to you.)

* `wmvembed` Allows you to create an embed for a Windows Media
  video from HMC's Windows Media Server.  Now (happily) defunct.


## License

These components are available for use under the terms of the GNU General Public License (GPL), version 2 or later.
