# Using Charts in HTML
![charts](http://www.coding-dude.com/wp/wp-content/uploads/2019/03/bar-chart-html-only.jpg)

Charts are far better for displaying data visually than tables and have the added benefit that no one is ever going to press-gang them into use as a layout tool. They’re easier to look at and convey data quickly, but they’re not always easy to create.

A great way to get started with charts is with Chart.js, a JavaScript plugin that uses HTML5’s canvas element to draw the graph onto the page. It’s a well documented plugin that makes using all kinds of bar charts, line charts, pie charts and more, incredibly easy.

To see how to use chart.js we’re going to create a set of 3 graphs; one will show the number of buyers a fictional product has over the course of 6 months, this will be a line chart; the second will show which countries the customers come from, this will be the pie chart; finally we’ll use a bar chart to show profit over the period.

## Setting up
The first thing we need to do is download Chart.js. Copy the Chart.min.js out of the unzipped folder and into the directory you’ll be working in. Then create a new html page and import the script:
<br>

`<!DOCTYPE html>`
`<html lang="en">`
`    <head>`
`        <meta charset="utf-8" />`
`        <title>Chart.js demo</title>`
`        <script src='Chart.min.js'></script>`
`   </head>`
 `   <body>`
`    </body>`
`</html>`

## Drawing a line chart
To draw a line chart, the first thing we need to do is create a canvas element in our HTML in which Chart.js can draw our chart. So add this to the body of our HTML page:

`<canvas id="buyers" width="600" height="400"></canvas>`

Next, we need to write a script that will retrieve the context of the canvas, so add this to the foot of your body element:

`Next, we need to write a script that will retrieve the context of the canvas, so add this to the foot of your body element:

`<script>`
`    var buyers = document.getElementById('buyers').getContext('2d');`
`    new Chart(buyers).Line(buyerData);`
`</script>`
<br>

(We can actually pass some options to the chart via the Line method, but we’re going to stick to the data for now to keep it simple.)

Inside the same script tags we need to create our data, in this instance it’s an object that contains labels for the base of our chart and datasets to describe the values on the chart. Add this immediately above the line that begins ‘var buyers=’:

`var buyerData = {`
`labels : ["January","February","March","April","May","June"],`
`	datasets : [`
`		{`
`			fillColor : "rgba(172,194,132,0.4)",`
`			strokeColor : "#ACC26D",`
`			pointColor : "#fff",`
`			pointStrokeColor : "#9DB86D",`
`			data : [203,156,99,251,305,247]`
`		}`
`	]`
`}`

> [Chart.js](https://www.chartjs.org/docs/latest/) docs: You’ll be needing these!


# The <canvas> element
`<canvas id="tutorial" width="150" height="150"></canvas>`

At first sight a <canvas> looks like the <img> element, with the only clear difference being that it doesn't have the src and alt attributes. Indeed, the <canvas> element has only two attributes, width and height. These are both optional and can also be set using DOM properties. When no width and height attributes are specified, the canvas will initially be 300 pixels wide and 150 pixels high. The element can be sized arbitrarily by CSS, but during rendering the image is scaled to fit its layout size: if the CSS sizing doesn't respect the ratio of the initial canvas, it will appear distorted.

>Note: If your renderings seem distorted, try specifying your width and height attributes explicitly in the `<canvas>` attributes, and not using CSS.

The id attribute isn't specific to the `<canvas>` element but is one of the global HTML attributes which can be applied to any HTML element (like class for instance). It is always a good idea to supply an id because this makes it much easier to identify it in a script.

The <canvas> element can be styled just like any normal image `(margin, border, background…)`. These rules, however, don't affect the actual drawing on the canvas. We'll see how this is done in a dedicated chapter of this tutorial. When no styling rules are applied to the canvas it will initially be fully transparent.


## Fallback content
The `<canvas>` element differs from an `<img>` tag in that, like for `<video>`, `<audio>`, or `<picture>` elements, it is easy to define some fallback content, to be displayed in older browsers not supporting it, like versions of Internet Explorer earlier than version 9 or textual browsers. You should always provide fallback content to be displayed by those browsers.

Providing fallback content is very straightforward: just insert the alternate content inside the <canvas> element. Browsers that don't support `<canvas>` will ignore the container and render the fallback content inside it. Browsers that do support `<canvas>` will ignore the content inside the container, and just render the canvas normally.

For example, we could provide a text description of the canvas content or provide a static image of the dynamically rendered content. This can look something like this:

>`<canvas id="stockGraph" width="150" height="150">`
 ` current stock price: $3.15 + 0.15`
`</canvas>`

>`<canvas id="clock" width="150" height="150">`
  `<img src="images/clock.png" width="150" height="150" alt=""/>`
`</canvas>`
