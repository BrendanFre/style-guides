# Style Guides
Style guides for various programming and mark-up languages that I use.
Last Updated: 10/07/2023
Updated by: Brendan Freeman

===================[TABLE OF CONTENTS]==================================

[HTML](#HTML)
[CSS3](#CSS3)
[JavaScript](#JavaScript)

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
│   ├── script.js
│
├── styles
│   ├── style.css
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

# CSS3

# JavaScript