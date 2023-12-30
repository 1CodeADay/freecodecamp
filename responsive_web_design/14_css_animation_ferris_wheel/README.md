# CHAP 14: Learn CSS Animation by Building a Ferris Wheel

You can use CSS animation to draw attention to specific sections of your webpage and make it more engaging.
In this course, you'll build a Ferris wheel. You'll learn how to use CSS to **animate** elements, **transform** them, and adjust their **speed**.

The **transform-origin property** is used to set the point around which a CSS transformation is applied. For example, when performing a rotate (which you will do later in this project), the transform-origin determines around which point the element is rotated.

Give the .line selector ***a transform-origin property of 0% 0%***. This will ***offset the origin point by 0% from the left and 0% from the top***, setting it to the top left corner of the element.

Create a selector to target your second .line element. Set the ***transform property to rotate(60deg)***.
You should create a **.line:nth-of-type(2) selector**.
Remember that the transform property allows you to manipulate the shape of an element. In this case, using the rotate(60deg) value will rotate the element around its transform-origin point by 60 degrees clockwise.

Set the transform property for the third .line to rotate(120deg), the fourth to rotate(180deg), the fifth to rotate(240deg), and the sixth to rotate(300deg).

Set the .cabin to have a transform-origin property of 50% 0%. This will set the origin point to be offset 50% from the left and 0% from the top, placing it in the middle of the top edge of the element.

Time to position the cabins around the wheel. Select the first .cabin element. Set the right property to -8.5% and the top property to 50%.

The **@keyframes at-rule** is used to define ***the flow of a CSS animation***. Within the @keyframes rule, you can create selectors for specific points in the ***animation sequence, such as 0% or 25%***, or use from and to to define the ***start and end*** of the sequence.

@keyframes rules require a name to be assigned to them, which you use in other rules to reference. For example, the @keyframes freeCodeCamp { } rule would be named freeCodeCamp. 

As an example, this would be a 12% rule:

@keyframes freecodecamp {
  12% {
    color: green;
  }
}

The **animation-name property** is used to link a @keyframes rule to a CSS selector. The value of this property should match the name of the @keyframes rule. Give your .wheel selector an animation-name property set to wheel.

The **animation-duration property** is used to set how long the animation should sequence to complete. The time should be specified in either seconds (s) or milliseconds (ms). Set your .wheel selector to have an animation-duration property of 10s.

The **animation-iteration-count property** sets how many times your animation should repeat. This can be set to a number, or to infinite to indefinitely repeat the animation. Your Ferris wheel should never stop, so set the .wheel selector to have an animation-iteration-count of infinite.

The **animation-timing-function property** sets how the animation should progress over time. There are a few different values for this property, but you want the Ferris wheel animation to run at the same rate from start to finish. Set the animation-timing-function to linear in your .wheel selector.

For your .cabin selector, you can use the animation property to set these all at once.

To make your cabin animation seem more like a ***natural swinging motion***, you can use the **ease-in-out timing function**. This setting will tell the animation to start and end at a slower pace, but move more quickly in the middle of the cycle.
Replace linear to ease-in-out in the .cabin selector.

Because the animation is on an infinite loop and the start and end colors are not the same, the transition appears jerky when it switches back to yellow from red.

