# CHAP 15: Learn CSS Transforms by Building a Penguin

You can transform HTML elements to create appealing designs that draw your reader's eye. ***You can use transforms to rotate elements, scale them***, and more.

In this course, you'll build a penguin. You'll use **CSS transforms to position and resize** the parts of your penguin, create a background, and animate your work.

Remove both the horizontal and vertical scrollbars, using only one property.
You should give body an **overflow of hidden**. 

To create some scenery in the background, you will add two mountains.
Above the .penguin element, add a div with a class of left-mountain.

To prevent the mountain from pushing the .ground element, adjust its position to prevent it from taking up space in the page layout.
You should give .left-mountain a position of absolute.

To make the mountain look more like a mountain, you can use the **skew transform function**, which takes two arguments. The ***first being an angle to shear the x-axis*** by, and the second being an angle to shear the y-axis by.

Set the ***stack level*** of the mountain element such that it remains directly behind the .ground element.
You should use the **z-index property** to change the stack level.

To overlap the mountain and .ground elements better, give the mountain a margin-top of 100px, and the .ground element a margin-top of -58px.

To give the effect of a mountain range, add another mountain

Position the sun in the top right corner of the screen such that 75px of its top and right edges are off screen.
You should give .sun a top and right of -75px

Most penguins do not have a square head.
Give the penguin a slightly oval head by setting the radius of the top corners to 70% and the radius of the bottom corners to 65%.

Target ***all descendent elements of the .penguin element***, and give them a position of absolute.
You should use the .penguin * selector.

To give the penguin body a crest, create a pseudo-element that is the first child of the .penguin-body element. Set the content property of the pseudo-element to an empty string.
.penguin-body::before

Position the pseudo-element relative to its closest positioned ancestor. 
Absolute

Round off the crest, by giving the pseudo-element bottom corners a radius of 100%, leaving the top corners at 0%.
  border-radius: 0% 0% 100% 100%;

In some browsers, the heart emoji may look slightly different from the previous step. ***This is because some of the character's properties were overridden by the font-weight style of bold.***
Fix this, by targeting the div with the heart emoji, and setting its ***font-weight to its original value***.
You should use the .shirt div selector to target the div with the heart emoji.
You should give the .shirt div a font-weight of initial or normal.


To keep the linear gradient on the correct side of the penguin's left arm, first rotate it by 130deg, then **invert the x-axis**.
You should give .arm.left a transform of rotate(130deg) **scaleX(-1)**.

Now, you are going to use CSS animations to make the penguin wave.
Define a new @keyframes named wave.

Retain the scaling of the left arm.
scaleX(-1)

Target the .penguin element when it is active, and ***increase its size*** by 50% in both dimensions.
.penguin:active {
  **transform: scale(1.5)**;
}

When you activate the .penguin element, it might look as though you can drag it around. This is not true.
Indicate this to users, by giving the active element a cursor property of not-allowed.