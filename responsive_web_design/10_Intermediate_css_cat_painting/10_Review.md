## Chap 10: Intermediate CSS by Building a Cat Painting
FCC 

**Mastering CSS positioning is essential for creating visually appealing and responsive web layouts.**
**In this course, you will build a cat painting. You'll learn about how to work with absolute positioning, the z-index property, and the transform property.**

**Box-sizing: border-box**  ensures elements include padding and border in their specified width and height.

To see the cat-head element, give it a linear gradient background with #5e5e5e at 85% and #45454f at 100%.
Your .cat-head selector should have a background property.
  *background: linear-gradient(#5e5e5e 85%, #45454f 100%)*

**CSS positioning** lets you set how you want an element to be positioned in the browser. It has a position property you can set to *static*, *absolute*, *relative*, *sticky* or *fixed*.
Once you set the position property of the element, you can move the element around by setting a pixel or a percentage value for one or more of the top, right, left, or bottom properties.
- **Static** is the default positioning for all elements. If you assign it to an element, you won't be able to move it around with top, right, left, or bottom.
- When you use the **relative** value, the element is still positioned according to the normal flow of the document, but the top, left, bottom, and right values become active.
- When you use the **absolute** value for your position property, the element is taken out of the normal flow of the document, and then its position is determined by the top, right, bottom, and left properties.
- **Fixed** is a position property value that lets you make an element fixed to the page no matter where the user scrolls to on the page.
- **Sticky** positioning is a hybrid of relative and fixed positioning. It allows an element to stick to a specific position within its containing element or viewport, based on the scroll position.

**Inset** is the shorthand for top, bottom, right and left.

Margin property on all sides to auto is one way to center an element vertically and horizontally using CSS positioning.

You are going to make each ear look like a triangle.
Using a class selector, give the .cat-left-ear element a left and right border of 35px solid transparent each. Also, set the bottom border to 70px solid #5e5e5e.

To position the left ear properly, you can use CSS transform to rotate it in a certain degree.
The **transform property** allows you to modify the shape, position, and size of an element without changing the layout or affecting the surrounding elements. It has functions such as **translate()**, **rotate()**, **scale()**, **skew()**, and **matrix()**.

The ears should always be placed above the part of the head it overlaps. You can do this with the z-index property.

**z-index** is a property you can use to define the **order of overlapping** HTML elements. Any element with a higher z-index will always be positioned over an element with a lower z-index.

Using a descendant selector, select the two div elements inside the div with class cat-mouth. 
You should have a .cat-mouth div selector.

You are going to make the two mouth lines into an **elliptical shape**. So, give the .cat-mouth div selector a border color of black transparent transparent transparent and a border radius of 190%/190px 150px 0 0.

