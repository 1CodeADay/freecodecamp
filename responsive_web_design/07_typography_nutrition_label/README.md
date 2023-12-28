# Chap 07: Learn Typography by Building a Nutrition Label

**Typography is the art of styling your text to be easily readable and suit its purpose.**
In this course, you'll use typography to build a nutrition label webpage. 
You'll learn how to style text, adjust line height, and position your text using CSS.

Within your head element, add a link element with the rel attribute set to stylesheet and the href attribute set to https://fonts.googleapis.com/css?family=Open+Sans:400,700,800.
This will import the Open Sans font family, with the font weight values 400, 700, and 800.

**Borders** can be used to group and prioritize content.

**Good use of white space can bring focus to the important elements** of your page, and help guide your user's eyes through your text.

If you inspect your .label element with your browser's developer tools, you may notice that it's actually 288 pixels wide instead of 270. This is because, by default, the browser includes the border and padding when determining an element's size.

Remember that the use of **h1, h2, and similar tags determine the semantic structure of your HTML**. However, you can adjust the CSS of these elements to control the visual flow and hierarchy.

**Lines can help separate and group important content**, especially when space is limited.

The **letter-spacing property** can be used to adjust the space between each character of text in an element.

Nutrition labels have a lot of bold text to draw attention to important information. Rather than targeting each element that needs to be bold, it is more efficient to use a class to apply the bold styling to every element.

**Horizontal spacing** between equally important elements can increase the readability of your text.

Now we can add the horizontal spacing using flex. In your p selector, add a display property set to flex and a justify-content property set to space-between.

**The rem unit stands for root em**, and is relative to the font size of the html element.

**Typography is often more art than science**. You may have to tweak things like alignment until it looks correct.

After your last .divider element, create a p element and give it the text Total Fat 8g 10%. Wrap the text Total Fat in a span element with the class of bold. Wrap the text 10% in another span element with the class of bold. Finally, nest the Total Fat span element and the text 8g in an additional span element for alignment.

**The :not pseudo-selector** can be used to select all elements that do not match the given CSS rule.
div:not(#example) {
  color: red;
}
The above selects all div elements without an id of example.