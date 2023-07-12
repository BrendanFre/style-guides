========================================================================
Project Name: Style Guides
Current Version: 0.2.0
Description: (Style guides for various programming and mark-up languages
that I use.
Creator: Brendan Freeman
Creation Date: 10 July 2023
Last Update By: Brendan Freeman
Last Updated Date: 12 July 2023
========================================================================

Last Updated: 12/07/2023
Updated by: Brendan Freeman

===================[TABLE OF CONTENTS]==================================

1. [HTML](#HTML)
2. [CSS3](#CSS3)
3. [JavaScript](#JavaScript)
4. [Markdown- README.md](#Markdown)

# HTML

## File Naming

Apart from the index.html file, all other HTML files should be named
according to their title tag. Limit to 2 words and should be joined by
a hyphen "-". The file names should remain lower case.

## Directory Structure

In the root directory there should only be 2 files, **index.html** and 
**.gitignore**. All other files should be stored in the relevant 
directories. 

```markdown
├── index.html
│
├── img
│   ├── image-1.jpg
│
├── pages
│   ├── page-1.html
│ 
├── scripts
│   ├── scripts.js
│
├── styles
│   ├── styles.css
│
└── .gitignore
```
img, pages, scripts, styles folders can have further sub directories add
ed if they have more than 5 files inside them. The sub directory names 
need to be descriptive and lower-case. 

## Mobile-First Approach

67% of web users according to https://www.oberlo.com/ use mobile to 
access the internet. By focusing on mobile first approach we can make 
the websites we design accessible for all. 
For navigation bars, we prefer to use a vertical list rather than a 
horizontal list. This can be accomplished with a drop-down.

For sections of the web page that will change depending on device,
add a comment to specify in what type of device the section will
appear.
```
<div id="dropdown">Click Me!
<!-- Visible by default: Desktop; Visible on click: Mobile -->
	<a href="link1.html>Link1</a>
	<a href="link2.html>Link2</a>
</div>
<!-- End of dynamic viewpoint -->
```

## Declare Document Type

**Always** declare the document type as per below.
```
<!DOCTYPE html>
```

## Declare the spoken language

**Always** declare the language of the text in the html tag:
```
<html lang="en">`
```
## Lower-case Element

**Always** use lower-case for elements, the only exception is the 
`<!DOCTYPE html>` and the value of attributes where the text must be
upper-case such as JavaScript functions.

## HTML Element Structure

When creating an element, make sure to close to close the element with 
a closing element:
```
<p>......</p>
```
For self-closing elements, before the end of the ">" use a forward slash
to signify self-closing:
```
<img />
```
When adding an attribute to the tag, there should be one space between
the element name and the attribute. Multiple attributes should also have
one space between them:

Good:
```
<element attribute="">
<element attribute="" attribute="">
```
Bad:
```
<elementattribute="">
<element  attribute=""attribute="">
```
There should never be a space between the attribute name, the equal sign
and the open quotes:

Good:
```
<element attribute="value">
<element attribute1="value1" attribute2="value2">
```
Bad:
```
<element attribute= "value">
<element attribute1 ="value1" attribute2 = "value2">
```

## HTML Semantics

Where possible use HTML semantics to define specific areas of the html
page. This is helpful for developers to clearly see where different
parts of the web page are located. It also has the added benefit for
assisting screen readers. Example of semantic tags:
```
<header>
<footer>
<nav>
<main>
```

## Div and Span

**Always** use the `<div>` tag when you need a section to take up a block
of a page. Always use `<span>` tags when you need a section to be
in-line. The only exception is when the requirements change between
desktop and mobile. In this case use a `<div>` tag and override
it's display property in the css file.

## Class Attribute

When assigning classes to an element, the element should only have one
class, unless frameworks and other external styles are used. Such as 
Bootstrap.

## ID Attribute

ID attribute should never be used for styling purposes. id attributes 
should be used to bookmark specific sections of the web page. This 
should be used for landing pages.
```
<!-- The link to the bookmark. -->
<a href="#reallycoolpart">Really cool link</a> 

<!-- Bookmarked section -->
<h2 id="reallycoolpart">Really Cool Part</h2>
```
Another use for id attribute is when targeting specific elements using
JavaScript such as a drop-down menu:
HTML file:
```
<span id="dropdown>I'm a dropdown</span>
```
JavaScript File:
```
...
getElementById("dropdown").style.display = "block";
...
```

## Linking CSS and JavaScript Files

CSS files should **always** be linked within the `<head>` element:

```
<head>
<link rel="stylesheet" href="/styles/styles.css">
</head>
```

JavaScript files should **always** be linked at the very end of the 
`<body>` element. This is to reduce initial load times, especially with 
bigger web pages with many images.

## HTML Skeleton

Here is the boilerplate for most types of webpages:
```
<!DOCTYPE html>
<html lang="en">
<head>
<title>Document Name</title>
<link rel="stylesheet" href="/styles/styles.css" />
</head>
<body>
	<header></header>
	<nav</nav>
	<main></main>
</body>
</html>
```

# CSS3

# JavaScript

# Markdown

Specifically readme files in repositories.

## Line Character Length

Markdown files should contain a maximum line character length of 72.
This makes the file easily readable on most devices. Only exception is
link addresses. 

## Header Section

All ReadMe markdown files should have a header section. This includes
information on what the readme file for. The creator, last updated by,
and dates. Such as Creation date and last update by date. The date
format should be dd mmm yyyy (example 12 July 2023).
```
========================================================================
Project Name: (Project name)
Current Version: (Version number based on this link 
https://semver.org/#:~:text=A%20normal%20version%20number%20MUST,0%20%2D%3E%201.11.0.
Description: (Short description of [project, maximum 2 lines)
Creator: (Initial creator name)
Creation Date: (Creation date)
Last Update By: (Last updater)
Last Updated Date: (Date it was last updated)
========================================================================
```