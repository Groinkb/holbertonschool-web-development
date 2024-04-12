# holbertonschool-web-development
Repository for holberton-school for fullstack specialisation


Nowadays developers tend to target less IDs in their CSS. The reason behind is that IDs should always be unique on a page. And for a maximum flexibility, the usage of only classes simplify the reusability of parts of the UI.

Cascading or order
* { } /* select all elements */
section /* select all section tags */
.my-class { } /* select all elements with that class */
.my-block > .my-title { }
.my-block + .my-title { }
.my-block ~ .my-title { }
#my-div /* select the element with that ID  */
Colors
The color CSS property sets the color value of a text HTML element.

Colors in CSS are represented most commontly represented by names, hexadecimal or RGB values.

Accessibility tip
When choosing colors for your design, you should always take accessibility into consideration. Modern browsers have now an easy way to show if a color is accessible or not

Code example
p { color: red; }
p { color: #f00; }
p { color: #ff0000; }
p { color: rgb(255,0,0); }
p { color: rgb(100%, 0%, 0%); }
p { color: hsl(0, 100%, 50%); }
Resources
color - CSS: Cascading Style Sheets | MDN
List of colors
Colors - A nicer color palette for the web.
Color Names — HTML Color Codes
CSS colour names
rgb(112, 128, 144) ✿ CSS.coloratum
CSS Variables
Custom properties or also called CSS variables represent custom properties that contain a value that can be reused across declarations.

Resources
var() - CSS: Cascading Style Sheets | MDN
Custom properties (–*): CSS variables - CSS: Cascading Style Sheets | MDN
Code example
:root {
  --main-bg-color: blue;
}
body {
  color: var(--main-bg-color);
}
Units and Values
Multiple CSS units can be used in your CSS. px (pixel) is the most used and an absolute lenght units, in contrast with relative lenght units.

Both (absolute and relative) are used in different contexts.

Rem: font size, padding, margin Em: media queries

Warning!
REM is relative to the root element: the <html> tag not <body> tag

Code example
font-size: 2rem;
padding: 1.2rem 2rem;
Resources
CSS values and units - Learn web development | MDN

Line-height
The line-height CSS property sets the height between lines of text.

Accessibility tip
Use a minimun of 1.5 for line-height for main paragraph content. It will help people with low vision conditions to easily read your content.

Resources
line-height - CSS: Cascading Style Sheets | MDN
Deep dive CSS: font metrics, line-height and vertical-align - Vincent De Oliveira
[How CSS line-height works and best practices - DEV Community ?‍??‍?]https://dev.to/lampewebdev/css-line-height-jjp)
Unitless line-heights – Eric’s Archived Thoughts
Code example
p {
    line-height: 1;
}
Text decoration
The text-decoration shorthand CSS property sets the appearance of decorative lines on text.

Resources
text-decoration - CSS: Cascading Style Sheets | MDN
Code example
a {
  text-decoration: line-through;
}
Text align
The text-align CSS property sets the horizontal alignment of a BLOCK element.

Resources
text-align - CSS: Cascading Style Sheets | MDN
Text transform
The text-transform CSS property allow to capitalize a text element.

Resources
text-transform - CSS: Cascading Style Sheets | MDN
Code example
p {
  text-transform: lowercase;
}
Letter spacing
The letter-spacing CSS property sets the spacing behavior between text characters.

Resources
letter-spacing - CSS: Cascading Style Sheets | MDN
Code example
a {
  letter-spacing: -0.4rem;
}
Pseudo Classes
A CSS pseudo-class is a keyword you can add to a selector. It specifies a different state of the element.

selector:pseudo-class {
  property: value;
}
Don’t confuse pseudo-classes with pseudo-elements. Pseudo-classes uses one : and pseudo-elements :: (it’s a way to distinguish both, even you could use single : for pseudo-elements).

Resources
Pseudo-classes - CSS: Cascading Style Sheets | MDN
:active - CSS: Cascading Style Sheets | MDN
:hover - CSS: Cascading Style Sheets | MDN
Code example
Always remember the LVHA-order or LoVe, HAte for Link, Visited, Hover, Active

/* a:link or just a */
a:link {
  color: green;
}
/* when you have already clicked and visited the link / page */
a:visited {
  color: cadetblue;
}
/* any link over which the user's pointer is hovering */
a:hover {
  text-decoration: underline;
}
a:active {
  color: darkcyan;
}
CSS Reset/Normalize
The expression CSS reset came from Eric Meyer who created a reset stylesheet in 2007, to reduce browser inconsistencies.

Since then, different solutions came out: Normalize.css, sanitize.css, reboot for Bootstrap…

Resources
CSS Tools: Reset CSS
Normalize CSS or CSS Reset?! - Elad Shechter - Medium
Reboot, Resets, and Reasoning | CSS-Tricks
HTML Kitchen-sink
Box Model
The box-model is one of the fundamental you need to understand. It’s the key to understand how to create layouts in CSS and how elements align in the page.



Resources
Introduction to the CSS basic box model - CSS: Cascading Style Sheets | MDN
width - CSS: Cascading Style Sheets | MDN
height - CSS: Cascading Style Sheets | MDN
padding - CSS: Cascading Style Sheets | MDN
margin - CSS: Cascading Style Sheets | MDN
Code example
/* This is the box-sizing by default */
.box {
  box-sizing: content-box;
}
/* This is the box-sizing value we usually use to create layouts */
.box {
  box-sizing: border-box;
}
/* This box has dimensions, padding and margin */
.box-dimensions {
  width: 100px;
  height: 50px;
  padding-top: 30px;
  margin: 5px;
}
CSS Flow and Display
Normal Flow, or Flow Layout, is the way that Block and Inline elements are displayed on a page before any changes are made to their layout.

Resources
CSS Flow Layout - CSS: Cascading Style Sheets | MDN
Block and inline layout in normal flow - CSS: Cascading Style Sheets | MDN
Grid System
Grid systems started to be used to layout books and magazines. They started to be used more recently to also create and define website’s layout. Before flexbox and css grid, grid systems were using floats to organize the content.

Warning
Before CSS Grid, developers were already using the word grid to define the responsive grid system used to build websites.

Resources
Floats Tutorial | HTML & CSS Is Hard
960 Grid System
What are Frameworks? 22 Best Responsive CSS Frameworks for Web Design
All About Floats | CSS-Tricks
Pseudo Elements
A CSS pseudo-element is a keyword added to a selector that lets you style a specific part of this element.

selector::pseudo-class {
  property: value;
}
Resources
Pseudo-elements - CSS: Cascading Style Sheets | MDN
::before and ::after pseudo-elements explained - DEV Community ?‍??‍?
::after (:after) - CSS: Cascading Style Sheets | MDN
A Single Div
A new micro clearfix hack – Nicolas Gallagher
Code example
/* Add an arrow as the last child of the link */
a::after {
  content: '→';
}
/* Change the font size of the first letter within all paragraphs */
p::first-letter {
  font-size: 130%;
}
Attribute Selectors
The attribute selectors allow you to target an attribute found on an HTML element.

Resources
Attribute selectors - CSS: Cascading Style Sheets | MDN
attribute CSS-Tricks
Splicing HTML’s DNA With CSS Attribute Selectors — Smashing Magazine
Attribute Selectors | Codrops CSS Reference
Code example
/* Links with "facebook" anywhere in the URL */
a[href*="facebook"] {
  color: #3C5A99;
}
/* Internal links, beginning with "#" */
a[href^="#"] {
  background-color: gold;
}
/* Links that end in ".org" */
a[href$=".org"] {
  color: red;
}
Background
Resources
background - CSS: Cascading Style Sheets | MDN
Code example
.box {
  background: ;
}
lineargradient
image
Borders
The border shorthand CSS property sets an element’s border.

Resources
border - CSS: Cascading Style Sheets | MDN
outline - CSS: Cascading Style Sheets | MDN
border-radius | CSS-Tricks
Code example
.box {
  display: block;
  padding: 1rem;
  border-width: 2px;
  border-style: double;
  border-color: orange;
  border-radius: 12px;
}
/* shorthand version */
.box {
  display: block;
  padding: 1rem;
  border-width: 2px double orange;
  border-radius: 12px;
}
Position
Positioning in CSS requires to use different CSS properties that allow you to position elements in your HTML webpage.

Resources
Positioning - CSS Reference
CSS Positioning 101 – A List Apart
A Detailed Look at the z-index CSS Property - Impressive Webs
position | CSS-Tricks
CSS Position Sticky - How It Really Works! - Elad Shechter - Medium
Code example
/* not 100% browser support yet, but could be user in some cases */
.component {
  position: sticky;
  top: 0;
}
CSS Transform
The transform CSS properties allow you to rotate, scale, skew, or translate an element.

Resources
transform - CSS: Cascading Style Sheets | MDN
CSS Transform Functions Visualizer
Code example
transform: perspective(17px);
transform: rotate3d(1, 2.0, 3.0, 10deg);
transform: translate(12px, 50%);
transform: scale(2, 0.5);
transform: skew(30deg, 20deg);
CSS Animation
The animation CSS properties allow you to animate other property of an element.

Warning!
Animation is a shorthand property. Only animation-duration and animation-name are required.

Resources
CSS Animations - CSS: Cascading Style Sheets | MDN
Using CSS animations - CSS: Cascading Style Sheets | MDN
Awesome CSS3 animation
Animate.css
The best CSS animation examples to recreate | Creative Bloq
Code example
@keyframes example {
  from {
    background-color: blue;
  }
  to {
    background-color: red;
  }
}
.box {
  width: 10rem;
  height: 10rem;
  background-color: blue;
  animation-name: example;
  animation-duration: 3s;
}
