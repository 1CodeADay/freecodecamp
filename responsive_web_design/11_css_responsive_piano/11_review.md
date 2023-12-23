## Chap 11: Learn Responsive Web Design by Building a Piano

**Responsive Design** tells your **webpage** how it should **look on different-sized screens**.
In this course, you'll use CSS and Responsive Design to code a piano. You'll also learn more about **media queries and pseudo selectors**.

Remember that a class attribute can have multiple values. To separate your white keys from your black keys, you'll add a second class value of black--key. 

Browsers can apply default margin and padding values to specific elements. To make sure your piano looks correct, you need to reset the box model.
Add an html rule selector to your CSS file, and set the box-sizing property to border-box.

Now that you have reset the html box model, you need to pass that on to the elements within as well. To do this, you can set the **box-sizing property to inherit**, which will tell the targeted elements to use the same value as the parent element.

You will also need to target the pseudo-elements, which are special keywords that follow a selector. The two pseudo-elements you will be using are the **::before** and **::after** pseudo-elements.

The ::before selector creates a pseudo-element which is the *first child of the selected element*, while the ::after selector creates a pseudo-element which is the last child of the selected element. *These pseudo-elements are often used to create cosmetic content*, which you will see later in this project.

For now, create a CSS selector to target all elements with *, and include the pseudo-elements with ::before and ::after. Set the box-sizing property to inherit.
*You should have a *, ::before, ::after selector.*

Give the .key a margin of 2px and a **float property** set to left.

Now it is time to use the pseudo-selectors you prepared for earlier. To create the black keys, add a new .key.black--key::after selector. This will target the elements with the class key black--key, and select the pseudo-element after these elements in the HTML.
In the new selector, set the background-color to #1d1e22. Also set the **content property to ""**. This will make the pseudo-elements empty.
The content property is used to set or override the content of the element. By default, the pseudo-elements created by the ::before and ::after pseudo-selectors are empty, and the elements will not be rendered to the page. Setting the content property to an empty string "" will ensure the element is rendered to the page while still being empty.

**The img element needs its parent to have a position set as a point of reference**. Set the position of the #piano selector to relative.

The **@media at-rule**, also known as a **media query**, is used to conditionally apply CSS. Media queries are commonly used to apply CSS based on the ***viewport width using the max-width and min-width properties***.
In the below example the padding is applied to the .card class when the viewport is 960px wide and below.
@media (max-width: 960px) {
  .card {
    padding: 2rem;
  }
}

You might have noticed the keys collapse when the browser window is smaller than 768px. **Set overflow to hidden** in the first .keys selector, to take care of this issue. This property will hide any element that is pushed outside the set width value of .keys.

**Logical operators** can be used to construct more complex media queries. The and logical operator is used to query two media conditions.
For example, a media query that targets a display width between 500px and 1000px would be:
@media (min-width: 500px) and (max-width: 1000px){
}







