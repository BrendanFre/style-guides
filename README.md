# Style Guides
Style guides for various programming and mark-up languages that I use.
Last Updated: 10/07/2023
Updated by: Brendan Freeman

===================[TABLE OF CONTENTS]==================================

1. [HTML](#HTML)
2. [CSS3](#CSS3)
3. [JavaScript](#JavaScript)

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
<html lang ="en">`
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
```
<!-- Good -->
<element attribute="">
<element attribute="" attribute="">

<!== Bad -->
<elementattribute="">
<element  attribute=""attribute="">
```
There should never be a space between the attribute name, the equal sign
and the open quotes:
```
<!-- Good -->
<element attribute="value">
<element attribute1="value1" attribute2="value2">

<!-- Bad -->
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

# CSS3

# JavaScript