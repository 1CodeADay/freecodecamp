# CHAP 13: Learn CSS Grid by building a magazine

In this course, you'll build a magazine article. You'll learn how to use CSS Grid, including concepts like ***grid rows and grid columns***.

Your three link elements should have a rel attribute with the value stylesheet.

The **loading attribute** on an img element can be set to **lazy** to tell the browser not to fetch the image resource until it is needed (as in, when the user scrolls the image into view). As an additional benefit, lazy loaded elements will not load until the non-lazy elements are loaded - this means users with slow internet connections can view the content of your page without having to wait for the images to load.

The **Referrer HTTP header** contains information about the address or URL of a page that a user might be visiting from. This information can be used in analytics to track how many users from your page visit freecodecamp.org, for example. Setting the rel attribute to noreferrer omits this information from the HTTP request. 

To start your CSS, normalize the CSS rules by targeting all elements with *, including the ::before and ::after pseudo-selectors.
***You should have a *, ::before, ::after selector.***

Create an html selector and give it a font-size property set to 62.5%. This will set the default font size for your web page to 10px (the browser default is 16px).

Create a body selector. Set the font-family property to Baskervville, with a fallback of serif. Set the color property to linen and the background-color property to rgb(20, 30, 40).

***CSS Grid offers a two-dimensional grid-based layout***, allowing you to center items horizontally and vertically while still retaining control to do things like overlap elements.

CSS Grid is similar to Flexbox in that it has a special property for both the parent and child elements.

**Grid-template-columns property** with a value of 1fr 94rem 1fr. This will create three columns where the middle column is 94rem wide, and the first and last columns are both **1 fraction** ***of the remaining space*** in the grid container.

***Use the minmax function to make your columns responsive on any device***. The minmax function takes two arguments, the first being the minimum value and the second being the maximum. These values could be a ***length, percentage, fr***, or even a keyword like max-content.
***grid-template-columns: minmax(2rem, 1fr) minmax(min-content, 94rem) minmax(2rem, 1fr);***

To add space between rows in the grid layout, you can use the **row-gap property**. 

One option is the **grid-column property**, which is shorthand for **grid-column-start** and **grid-column-end**. The grid-column property tells the grid item which grid line to start and end at.

Set the grid-column property to 2 / 3. This will tell the .heading element to start at grid line 2 and end at grid line 3.

For additional control over the layout of your content, you can have a CSS Grid within a CSS Grid.


The CSS **repeat() function** is used to repeat a value, rather than writing it out manually, and is helpful for grid layouts. For example, setting the grid-template-columns property to ***repeat(20, 200px)*** would create ***20 columns each 200px wide***.

Remember that the ***grid-column property determines which columns an element starts and ends at***. There may be times where you are unsure of how many columns your grid will have, but you want an element ***to stop at the last column***. To do this, ***you can use -1 for the end column***.

The **object-fit property** tells the browser how to position the element within its container. In this case, **cover** will set the image to fill the container, cropping as needed to avoid changing the aspect ratio.

The default settings for CSS Grid will create additional rows as needed, unlike Flexbox. Give the .social-icons selector a grid-template-columns property set to repeat(5, 1fr) to arrange the icons in a single row.

If you wanted to add more social icons, but keep them on the same row, you would need to update grid-template-columns to create additional columns. As an alternative, you can use the **grid-auto-flow property**.

This property takes either ***row or column as the first value***, with an ***optional second value of dense***. grid-auto-flow uses an auto-placement algorithm to adjust the grid layout. ***Setting it to column will tell the algorithm to create new columns for content as needed.*** The dense value allows the algorithm to backtrack and fill holes in the grid with smaller items, which can result in items appearing out of order.

***The algorithm defaults the new column width to be auto***, which will not match your current columns.
You can override this with the grid-auto-columns property. 

Much like Flexbox, with CSS Grid you can align the content of grid items with align-items and justify-items. align-items will align child elements along the column axis, and justify-items will align child elements along the row axis.

Your .text element is not a CSS Grid, but you can ***create columns within an element without using Grid by using the column-width property***.

Magazines often use justified text in their printed content to structure their layout and control the flow of their content. While this works in printed form, justified text on websites can be an accessibility concern, for example presenting challenges for folks with dyslexia. 

To make your project look like a printed magazine, give the .text selector a text-align property set to justify.

The **::first-letter pseudo-selector** allows you to target the first letter in the text content of an element.
Create a .first-paragraph::first-letter

The other text has been shifted out of place. Move it into position by giving the .first-paragraph::first-letter selector a **float property** set to left and a margin-right property set to 1rem.

A quote is not really a quote without proper quotation marks. You can add these with CSS pseudo selectors.
Create a ***.quote::before*** selector and set the content property to ***" with a space following it***.
Also, create a .quote::after selector and set the content property to " with a space preceding it.

Grid-template-columns property set to 2fr 1fr and a grid-template-rows property set to repeat(3, min-content). This will give our grid rows that adjust in height based on the content, but columns that remain a fixed width based on the container.

The **gap property** is a shorthand way to set the value of column-gap and row-gap at the same time. If given one value, it sets the column-gap and row-gap both to that value. If given two values, it sets the row-gap to the first value and the column-gap to the second.

The **place-items property** can be used to set the align-items and justify-items values at the same time. The place-items property takes one or two values. If one value is provided, it is used for both the align-items and justify-items properties. If two values are provided, the first value is used for the align-items property and the second value is used for the justify-items property.

Grid-column property set to 1 / -1. This will allow the first and third images to span the full width of the grid.

Now that the magazine layout is finished, you need to make it responsive.

Start with a @media query for only screen with a max-width of 720px. Inside, create an .image-wrapper selector and give it a grid-template-columns property of 1fr.

This will collapse the three images into one column on smaller screens.
You should have a new @media rule for only screen and (max-width: 720px).






<p class=""></p>

<section class=""></section>

<article class=""></article>

<aside class=""></aside>

<h3 class="list-title"></h3>
<ul></ul>

<hr>