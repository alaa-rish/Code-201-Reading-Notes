# Introduction for HTML & CSS

### Quick tip: HTML tags

Before you dive into the challenge, here's a quick review of HTML tags:
![htmltag](https://cdn.kastatic.org/ka-perseus-images/2b914caea7fdf9df8ff30e4780096d38624cab4f.png)

The closing tag always comes after the content of the tag - it's how the browser knows that you want the tag to end.
The contents of an HTML tag are the stuff that goes between the opening and closing tags - this is what we mean when we say "inside" a tag. The contents of a tag can be normal text or a mix of other tags.

### Where should your tags go?
Any content that is visible on your web page should go between the opening <body> tag and the closing </body> tag, like in the screenshot below:
![](https://cdn.kastatic.org/ka-perseus-images/a88dceb91dbddc6f1c031bf92bedb90afca3ff05.png)

The (**< h1 >**) and (**< p >**) tags are the contents of the (**< body >**) tag, so we say they're "inside" the <body> tag. In fact, those tags must go inside the <body> tag, so remember that when you're writing your HTML in your first challenge. Try it out now!
  
  
  ### Quick tip: Selecting by tag name
  As you just learned, we use CSS rules to select elements on a web page so that we can then style those elements.
The way we tell our CSS rule which HTML elements to style is by using selectors. There are many types of selectors that we'll cover later, but here we just want to review the one we showed in the talk-through: the element selector.
The element selector selects HTML elements based on their tag names. Each HTML element—(< h1 >), (< p >), (< li >), (< body >)—and any other HTML element can be selected with CSS by using the tag name without the angle brackets (< and >). For example, you can select all of the (< p >) tags in your webpage by using the element selector p. Here's a CSS rule that changes the color of each paragraph on a web page:

  
