# CHAP 12: Learn CSS Variables by Building a City Skyline.

CSS variables help you organize your styles and reuse them.
In this course, you'll build a city skyline. You'll learn how to configure CSS variables so you can reuse them whenever you want.

In CSS, you can **target everything with an asterisk**. Add a border to everything by using the * selector, and giving it a border of 1px solid black. This is a trick that helps visualize where elements are and their size. 

Center the parts of your building by turning the .bb1 element into a Flexbox parent. Use the flex-direction and align-items properties to center the children.

Variable declarations begin with two dashes (-) and are given a name and a value like this: --variable-name: value;

To use a variable, put the variable name in parentheses with var in front of them like this: var(--variable-name). Whatever value you gave the variable will be applied to whatever property you use it on.
**background-color: var(--building-color1);**

The main advantage of using variables is being able to quickly change many values in your stylesheet by just changing the value of a variable.

The buildings are currently stacked on top of each other. Align the buildings by turning the .background-buildings element into a flexbox parent. Use the align-items and justify-content properties to evenly space the buildings across the bottom of the element.
    display: flex;
    align-items: flex-end;
    justify-content: space-evenly;

The buildings are too spaced out. Squeeze them together by adding two empty div elements to the top of the .background-buildings element, two more at the bottom of it, and one more in between .bb3 and .bb4. These will be added as evenly-spaced elements across the container, effectively moving the buildings closer to the center.

**You should add a fallback value** to a variable by putting it as the second value of where you use the variable like this: var(--variable-name, fallback-value). The property will use the fallback value when there's a problem with the variable.

The variables you declared in .bb1 do not cascade to the .bb2 and .bb3 sibling elements. That's just how CSS works. Because of this, **variables are often declared in the :root selector**. 

***This is the highest level selector in CSS***; putting your variables there will make them usable everywhere. Add the :root selector to the top of your stylesheet, and move all your variable declarations there.

***You should optimize your code***. Move the position and top properties and values from .foreground-buildings to .background-buildings. Then select both .background-buildings and .foreground-buildings there, effectively applying those styles to both of the elements. You can use a comma (,) to separate selectors like this: selector1, selector2.

Move the position of .fb4 relative to where it is now by adding a position of relative and left of 10% to it. Do the same for .fb5 but use right instead of left. This will cover up the remaining white space in between the buildings.

Comments in CSS look like this: /* Comment here */.

**Gradients in CSS are a way to transition between colors** across the distance of an element. They are applied to the background property and the syntax looks like this:
    gradient-type(
    color1,
    color2
    );
In the example, color1 is solid at the top, color2 is solid at the bottom, and in between it transitions evenly from one to the next. 
***background: linear-gradient(var(--building-color1), var(--window-color1));***

Gradients can use as many colors as you want like this:

You can ***specify where you want a gradient transition to complete*** by adding it to the color like this:
    gradient-type(
    color1,
    color2 20%,
    color3
    );

Gradient transitions often gradually change from one color to another. You can make the change a solid line like this:
linear-gradient(
  var(--first-color) 0%,
  var(--first-color) 40%,
  var(--second-color) 40%,
  var(--second-color) 80%
);

You can see the hard color change at the top of the section. Change the gradient type from linear-gradient to **repeating-linear-gradient** for this section. This will make the four colors of your gradient repeat until it gets to the bottom of the element; ***giving you some stripes, and saving you from having to add a bunch of elements to create them.***

Create and add the following properties to .bb2a:
    margin: auto;
    width: 5vw;
    height: 5vw;
    border-top: 1vw solid #000;
    border-bottom: 1vw solid #000;
    border-left: 1vw solid #999;
    border-right: 1vw solid #999;
After you add these, you can see how a thick border on an element gives you some angles where two sides meet. You are going to use that bottom border as the top of the building.

Remove the width and height from .bb2a, and change the border-left and border-right to use 5vw instead of 1vw. ***The element will now have zero size and the borders will come together in the middle.***

Remove the margin and border-top properties and values from .bb2a to turn it into a triangle for the top of the building.

All the gradients you created have gone from top to bottom, that's the default direction. You can specify another direction by adding it before your colors like this:
    gradient-type(
    direction,
    color1,
    color2
    );
Use 90deg for the direction, your building-color3 for the first two colors, and window-color3 at 15% for the third. When you don't specify a distance for a color, it will use the values that makes sense. In this case, the first two colors will default to 0% and 7.5% because it starts at 0%, and 7.5% is half of the 15%.

You can add multiple gradients to an element by separating them with a comma (,) like this:
    gradient1(
    colors
    ),
    gradient2(
    colors
    );

This will put a 7vh height border on the bottom. But since the element has zero size, it only shows up as a 2px wide line from the 1px border that is on all the elements.

***When you increase the size of the left and right borders, the border on the bottom will expand to be the width of the combined left and right border widths. ***

They will be invisible, but it will make the border on the bottom ..... wide.

With CSS variables you can change values without searching everywhere in the stylesheet. 

The windows are stacked on top of each other on the rightmost purple building. Turn the building into a flexbox parent, and use the flex-wrap property to put the windows side by side, and push them down to a new row when they don't fit.

At the top of the sky gradient color list, where you would put a direction for the gradient; add circle closest-corner at 15% 15%,. This will move the start of the gradient to 15% from the top and left. It will make it end at the closest-corner and it will maintain a circle shape. 

You are going to make another color scheme for the skyline that changes it from day to night.

**Variables are primarily used with colors**, and that's how you used them here. 

