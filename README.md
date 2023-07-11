# CoreModuleAssign2




# Answer 1>
The CSS box model is essentially a box that wraps around every HTML element. It consists of: margins, borders, padding, and the actual content.

# Answer 2>
CSS selectors are used to "find" (or select) the HTML elements you want to style.

We can divide CSS selectors into five categories:

## Simple selectors (select elements based on name, id, class)
### Eg,
```
p {
  text-align: center;
  color: red;
}

#para1 {
  text-align: center;
  color: red;
}
.center {
  text-align: center;
  color: red;
}
```

## Combinator selectors (select elements based on a specific relationship between them)
It has following types -
Descendant Selector
The descendant selector matches all elements that are descendants of a specified     element.

The following example selects all <p> elements inside <div> elements:

### Eg. 
```
div p {
  background-color: yellow;
}
```

##  Child Selector (>)
The child selector selects all elements that are the children of a specified element.
The following example selects all <p> elements that are children of a <div> element:

### Eg.
```
div > p {
  background-color: yellow;
}
```

## Adjacent Sibling Selector (+)
The adjacent sibling selector is used to select an element that is directly after another specific element.

Sibling elements must have the same parent element, and "adjacent" means "immediately following".

The following example selects the first <p> element that are placed immediately after <div> elements:

### Eg.
```
div + p {
  background-color: yellow;
}
```
## General Sibling Selector (~)
The general sibling selector selects all elements that are next siblings of a specified element.

The following example selects all <p> elements that are next siblings of <div> elements:


```
Eg. div ~ p {
  background-color: yellow;
}
```

## Pseudo-class selectors (select elements based on a certain state)
A pseudo-class is used to define a special state of an element.

For example, it can be used to:

Style an element when a user mouses over it
Style visited and unvisited links differently
Style an element when it gets focus

## Pseudo-elements selectors (select and style a part of an element)

### Eg.
```
/* unvisited link */
a:link {
  color: #FF0000;
}

/* visited link */
a:visited {
  color: #00FF00;
}

/* mouse over link */
a:hover {
  color: #FF00FF;
}

/* selected link */
a:active {
  color: #0000FF;
}
```
## Attribute selectors (select elements based on an attribute or attribute value)

It is possible to style HTML elements that have specific attributes or attribute values.

CSS [attribute] Selector
The [attribute] selector is used to select elements with a specified attribute.

The following example selects all <a> elements with a target attribute:

Eg. a[target] {
  background-color: yellow;
}

Answer 3 > 
VW/VH is relative length
Relative length units specify a length relative to another length property. Relative length units scale better between different rendering medium.

vw : Relative to 1% of the width of the viewport*
vh:  Relative to 1% of the height of the viewport*

Px is absolute length

The absolute length units are fixed and a length expressed in any of these will appear as exactly that size.

px: pixels (1px = 1/96th of 1in)

Answer 4 >

Block element 

A block element always starts on a new line, and fills up the horizontal space left and right on the web page. You can add margins and padding on all four sides of any block element — top, right, left, and bottom.

Inline Element

Inline elements don’t start on a new line, they appear on the same line as the content and tags beside them. Some examples of inline elements are <span> , <strong>, and <img> tags.

Inline - Block

Inline-block elements are similar to inline elements, except they can have padding and margins added on all four sides. You’ll have to declare display: inline-block in your CSS code.




Answer 5>
content-box: This is the default value of box-sizing. The dimension of element only includes ‘height’ and ‘width’ and does not include ‘border’ and ‘padding’ given to element. Padding and Border take space outside the element.

border-box: In this value, not only width and height properties are included but you will find padding and border inside of the box for example .box {width: 200px; border: 10px solid black;} renders a box that is 200px wide.

Answer 6 > 

Z Index (z-index) is a CSS property that defines the order of overlapping HTML elements. Elements with a higher index will be placed on top of elements with a lower index.

Note: Z index only works on positioned elements (position:absolute, position:relative, or position:fixed).

Possible Values
/* Default value if not specified */
z-index: auto;

/* Integer values */
z-index: 1;
z-index: 100;
z-index: 9999;
z-index: -1;

/* Global values */
z-index: inherit;
z-index: initial;
z-index: unset

Usage:
<!DOCTYPE html>
<html>
<head>
<style>
body {
  background-color:#E7E9EB;
}
#myDIV {
  width:100%;
  position:absolute;
  height:300px;
  background-color:#FFFFFF;
}
#myDIV div{
  width:100px;
  height:100px;
  position:absolute;
  background-color:yellow;
  border:1px solid;
  opacity:0.5;
}
#myBox {
  position:absolute;
  background-color:red!important;
  opacity:1!important;
  z-index: 2;
}
</style>
</head>
<body>

<h1>The z-index property</h1>

<div id="myDIV">
  <div id="myBox">myBox</div>
  <div style="top:20px;left:20px;z-index:0;">z-index 0</div>
  <div style="top:40px;left:40px;z-index:1;">z-index 1</div>
  <div style="top:60px;left:60px;z-index:2;">z-index 2</div>        
  <div style="top:80px;left:80px;z-index:3;">z-index 3</div>            
</div>

</body>
</html>

Answer 6 > 

CSS Grid : The CSS Grid Layout is a two-dimensional grid-based layout system with rows and columns. It is useful in creating more complex and organized layouts.

To define a grid container, you will have to pass a display: grid property to your element.

 CSS Flexbox: It is a one-dimensional layout. It is useful in allocating and aligning the space among items in a grid container. It works with various kinds of display devices and screen sizes. Flex layout makes it easier to design and build responsive web pages without using many float and position properties in the CSS code.

To start using Flexbox, you have to create a flex container using the display: flex property. Every element inside the particular flex container will act as a flex item.

One vs. Two Dimension

Flexbox is made for one-dimensional layouts, and the Grid is made for two-dimensional layouts. It means Flexbox can work on either rows or columns at a time, but Grids can work on both.

Answer 7 >
 Absolute
This is a very powerful type of positioning that allows you to literally place any page element exactly where you want it. You use the positioning attributes top, left, bottom, and right to set the location. Remember that these values will be relative to the next parent element with relative (or absolute) positioning. If there is no such parent, it will default all the way back up to the <html> element itself meaning it will be placed relative to the page itself.

Relative
This type of positioning is probably the most confusing and misused. What it really means is “relative to itself”. If you set position: relative; on an element but no other positioning attributes (top, left, bottom or right), it will have no effect on it’s positioning at all, it will be exactly as it would be if you left it as position: static; But if you do give it some other positioning attribute, say, top: 10px;, it will shift its position 10 pixels down from where it would normally be. I’m sure you can imagine, the ability to shift an element around based on its regular position is pretty useful.

Fixed
A fixed position element is positioned relative to the viewport, or the browser window itself. The viewport doesn’t change when the window is scrolled, so a fixed positioned element will stay right where it is when the page is scrolled.

Sticky

Sticky positioning is a hybrid of relative and fixed positioning. The element is treated as relative positioned until it crosses a specified threshold, at which point it is treated as fixed positioned.

Answer 8> Link

Answer 9 > Link

Answer 10 > Please checkout my paytm clone which is desktop, mobile as well as tablet responsive - Link
