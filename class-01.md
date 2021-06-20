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
  
  
  ### What is CSS? And How Does It Relate to HMTL?
  
  CSS stands for Cascading Style Sheets with an emphasis placed on “Style.” While HTML is used to structure a web document (defining things like headlines and paragraphs, and allowing you to embed images, video, and other media), CSS comes through and specifies your document’s style—page layouts, colors, and fonts are all determined with CSS. Think of HTML as the foundation (every house has one), and CSS as the aesthetic choices (there’s a big difference between a Victorian mansion and a mid-century modern home).

####How Does CSS Work?
CSS brings style to your web pages by interacting with HTML elements. Elements are the individual HTML components of a web page—for instance a paragraph—which in HTML might look like this:

<p>This is my paragraph!</p>
If you wanted to make this paragraph appear pink and bold to people viewing your web page through a web browser, you’d use CSS code that looks like this:

p  {  color:pink;  font-weight:bold;  }
In this case, “p” (the paragraph) is called the “selector”—it’s the part of CSS code specifying which HTML element the CSS styling will effect. In CSS, the selector is written to the left of the first curly bracket. The information between curly brackets is called a declaration, and it contains properties and values that are applied to the selector. Properties are things like font size, color, and margins, while values are the settings for those properties. In the example above, “color” and “font-weight” are both properties, and “pink” and “bold” are values. The full bracketed set of

{  color:pink;  font-weight:bold;  } 
is the declaration, and again, “p” (meaning the HTML paragraph) is the selector. These same basic principles can be applied to change font sizes, background colors, margin indentations, and more. For instance. . .

body  {  background-color:lightblue;  }
. . .would make your page’s background light blue, or. . .

p  {  font-size:20px;  color:red;  }
. . .will create a 20 point font paragraph with red letters.

#### External, Internal, or Inline CSS?
You might be wondering how this CSS code is actually applied to HTML content, though. Much like HTML, CSS is written in simple, plain text through a text editor or word processor on your computer, and there are three main ways to add that CSS code to your HTML pages. CSS code (or Style Sheets) can be external, internal, or inline. External style sheets are saved as .css files and can be used to determine the appearance of an entire website through one file (rather than adding individual instances of CSS code to every HTML element you want to adjust). In order to use an external style sheet, your .html files need to include a header section that links to the external style sheet and looks something like this:

<head>
<link rel=”stylesheet”  type=”text/css”  href=mysitestyle.css”>
</head>
This will link the .html file to your external style sheet (in this case, mysitestyle.css), and all of the CSS instructions in that file will then apply to your linked .html pages.

Internal style sheets are CSS instructions written directly into the header of a specific .html page. (This is especially useful if you have a single page on a site that has a unique look.) An internal style sheet looks something like this. . .

<head>
<style>
Body  {  background-color:thistle;  }
P  {  font-size:20px;  color:mediumblue;  }
</style>
</head>
. . . a thistle background color and paragraphs with 20 point, medium blue font will now be applied to this single .html page.

Finally, inline styles are snippets of CSS written directly into HTML code, and applicable only to a single coding instance. For example: 
  (<h1  style= ” font-size:40px;color:violet;”>Check out this headline!</h1>)
  
  
would cause one specific headline on a single .html page to appear in violet, 40 point font.

Generally speaking, external style sheets are the most efficient method for implementing CSS on a website (it’s easier to keep track of and implement a site’s style from a dedicated CSS file), while internal style sheets and inline style can be used on a case by case basis when individual style changes need to be made.

So if HTML is the foundation, frames, walls, and girders supporting your website, consider CSS the paint color, window styles, and landscaping that comes on afterward. You can’t get anywhere without putting that foundation up first, but—once you do—you’ll want to follow up with some style, and CSS is the ticket to unleashing your inner decorator.
  
  

  
