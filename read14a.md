# CSS Transforms, Transitions, and Animations
---
![ANIMATION](https://www.thespian.hr/png/bringing-web-pages-to-life-css-animations.png)
## Transforms
With CSS3 came new ways to position and alter elements. Now general layout techniques can be revisited with alternative ways to size, position, and change elements. All of these new techniques are made possible by the transform property.

The transform property comes in two different settings, two-dimensional and three-dimensional. Each of these come with their own individual properties and values.

Within this lesson we’ll take a look at both two-dimensional and three-dimensional transforms. Generally speaking, browser support for the transform property isn’t great, but it is getting better every day. For the best support vendor prefixes are encouraged, however you may need to download the nightly version of Chrome to see all of these transforms in action.

## Transform Syntax
The actual syntax for the transform property is quite simple, including the transform property followed by the value. The value specifies the transform type followed by a specific amount inside parentheses.

`div {`
 ` -webkit-transform: scale(1.5);`
  `   -moz-transform: scale(1.5);`
   `    -o-transform: scale(1.5);`
    `      transform: scale(1.5);`
`}`

Notice how the transform property includes multiple vendor prefixes to gain the best support across all browsers. The un-prefixed declaration comes last to overwrite the prefixed versions, should a browser fully support the transform property.

In the interest of brevity, the remainder of this lesson will not include vendor prefixes. They are, however, strongly encouraged for any code in a production environment. Over time we will be able to remove these prefixes, however keeping them in is the safest approach for the time being.

## 2D Transforms
Elements may be distorted, or transformed, on both a two-dimensional plane or a three-dimensional plane. Two-dimensional transforms work on the x and y axes, known as horizontal and vertical axes. Three-dimensional transforms work on both the x and y axes, as well as the z axis. These three-dimensional transforms help define not only the length and width of an element, but also the depth. We’ll start by discussing how to transform elements on a two-dimensional plane, and then work our way into three-dimensional transforms.

## 2D Rotate
The transform property accepts a handful of different values. The rotate value provides the ability to rotate an element from 0 to 360 degrees. Using a positive value will rotate an element clockwise, and using a negative value will rotate the element counterclockwise. The default point of rotation is the center of the element, 50% 50%, both horizontally and vertically. Later we will discuss how you can change this default point of rotation.


### HTML
`<figure class="box-1">Box 1</figure>`
`<figure class="box-2">Box 2</figure>`


### CSS
`.box-1 {`
` transform: rotate(20deg);`
`}`
`.box-2 {`
`  transform: rotate(-55deg);`
`}`

## 2D Scale
Using the scale value within the transform property allows you to change the appeared size of an element. The default scale value is 1, therefore any value between .99 and .01 makes an element appear smaller while any value greater than or equal to 1.01 makes an element appear larger.

### HTML
`<figure class="box-1">Box 1</figure>`
`<figure class="box-2">Box 2</figure>`

              
### CSS
`.box-1 {`
`  transform: scale(.75);`
`}`
`.box-2 {`
`  transform: scale(1.25);`
`}`

              

It is possible to scale only the height or width of an element using the scaleX and scaleY values. The scaleX value will scale the width of an element while the scaleY value will scale the height of an element. To scale both the height and width of an element but at different sizes, the x and y axis values may be set simultaneously. To do so, use the scale transform declaring the x axis value first, followed by a comma, and then the y axis value.

### HTML
`<figure class="box-1">Box 1</figure>`
`<figure class="box-2">Box 2</figure>`
`<figure class="box-3">Box 3</figure>`

              
### CSS
`.box-1 {`
`  transform: scaleX(.5);`
`}`
`.box-2 {`
`  transform: scaleY(1.15);`
`}`
`.box-3 {`
`  transform: scale(.5, 1.15);`
`}`
---

# Transitions & Animations
One evolution with CSS3 was the ability to write behaviors for transitions and animations. Front end developers have been asking for the ability to design these interactions within HTML and CSS, without the use of JavaScript or Flash, for years. Now their wish has come true.

With CSS3 transitions you have the potential to alter the appearance and behavior of an element whenever a state change occurs, such as when it is hovered over, focused on, active, or targeted.

Animations within CSS3 allow the appearance and behavior of an element to be altered in multiple keyframes. Transitions provide a change from one state to another, while animations can set multiple points of transition upon different keyframes.

## Transitions#transitions
As mentioned, for a transition to take place, an element must have a change in state, and different styles must be identified for each state. The easiest way for determining styles for different states is by using the :hover, :focus, :active, and :target pseudo-classes.

There are four transition related properties in total, including transition-property, transition-duration, transition-timing-function, and transition-delay. Not all of these are required to build a transition, with the first three are the most popular.

In the example below the box will change its background color over the course of 1 second in a linear fashion.
`.box {`
`  background: #2db34a;`
 ` transition-property: background;`
`  transition-duration: 1s;`
`  transition-timing-function: linear;`
`}`
`.box:hover {`
`  background: #ff7b29;`
`}`


## Transitional Property
The transition-property property determines exactly what properties will be altered in conjunction with the other transitional properties. By default, all of the properties within an element’s different states will be altered upon change. However, only the properties identified within the transition-property value will be affected by any transitions.

In the example above, the background property is identified in the transition-property value. Here the background property is the only property that will change over the duration of 1 second in a linear fashion. Any other properties included when changing an element’s state, but not included within the transition-property value, will not receive the transition behaviors as set by the transition-duration or transition-timing-function properties.

If multiple properties need to be transitioned they may be comma separated within the transition-property value. Additionally, the keyword value all may be used to transition all properties of an element.

`.box {`
`    background: #2db34a;`
`    border-radius: 6px`
`    transition-property: background, border-radius;`
`    transition-duration: 1s;`
`    transition-timing-function: linear;`
`  }`
`  .box:hover {`
`    background: #ff7b29;`
`    border-radius: 50%;`
`  }`

## Transition Duration
The duration in which a transition takes place is set using the transition-duration property. The value of this property can be set using general timing values, including seconds (s) and milliseconds (ms). These timing values may also come in fractional measurements, .2s for example.

When transitioning multiple properties you can set multiple durations, one for each property. As with the transition-property property value, multiple durations can be declared using comma separated values. The order of these values when identifying individual properties and durations does matter. For example, the first property identified within the transition-property property will match up with the first time identified within the transition-duration property, and so forth.

If multiple properties are being transitioned with only one duration value declared, that one value will be the duration of all the transitioned properties.

`.box {`
`  background: #2db34a;`
`  border-radius: 6px;`
`  transition-property: background, border-radius;`
`  transition-duration: .2s, 1s;`
`  transition-timing-function: linear;`
`}`
`.box:hover {`
`  background: #ff7b29;`
`  border-radius: 50%;`
`}`

## Transition Timing
The transition-timing-function property is used to set the speed in which a transition will move. Knowing the duration from the transition-duration property a transition can have multiple speeds within a single duration. A few of the more popular keyword values for the transition-timing-function property include linear, ease-in, ease-out, and ease-in-out.

The linear keyword value identifies a transition moving in a constant speed from one state to another. The ease-in value identifies a transition that starts slowly and speeds up throughout the transition, while the ease-out value identifies a transition that starts quickly and slows down throughout the transition. The ease-in-out value identifies a transition that starts slowly, speeds up in the middle, then slows down again before ending.

Each timing function has a cubic-bezier curve behind it, which can be specifically set using the cubic-bezier(x1, y1, x2, y2) value. Additional values include step-start, step-stop, and a uniquely identified steps(number_of_steps, direction) value.

When transitioning multiple properties, you can identify multiple timing functions. These timing function values, as with other transition property values, may be declared

`.box {`
`  background: #2db34a;`
`  border-radius: 6px;`
`  transition-property: background, border-radius;`
`  transition-duration: .2s, 1s;`
`  transition-timing-function: linear, ease-in;`
`}`
`.box:hover {`
`  background: #ff7b29;`
`  border-radius: 50%;`
`}`

## Transition Delay
On top of declaring the transition property, duration, and timing function, you can also set a delay with the transition-delay property. The delay sets a time value, seconds or milliseconds, that determines how long a transition should be stalled before executing. As with all other transition properties, to delay numerous transitions, each delay can be declared as comma separated values.

`.box {`
`  background: #2db34a;`
`  border-radius: 6px`
`  transition-property: background, border-radius;`
`  transition-duration: .2s, 1s;`
`  transition-timing-function: linear, ease-in;`
`  transition-delay: 0s, 1s;`
`}`
`.box:hover {`
`  background: #ff7b29;`
`  border-radius: 50%;`
`}`


## Shorthand Transitions#shorthand-transitions
Declaring every transition property individually can become quite intensive, especially with vendor prefixes. Fortunately there is a shorthand property, transition, capable of supporting all of these different properties and values. Using the transition value alone, you can set every transition value in the order of transition-property, transition-duration, transition-timing-function, and lastly transition-delay. Do not use commas with these values unless you are identifying numerous transitions.

To set numerous transitions at once, set each individual group of transition values, then use a comma to separate each additional group of transition values.

`.box {`
  background: #2db34a;`
`  border-radius: 6px;`
`  transition: background .2s linear, border-radius 1s ease-in 1s;`
`}`
`.box:hover {`
`  color: #ff7b29;`
`  border-radius: 50%;`
`}`

## Transitional Button
### HTML
`<button>Awesome Button</button>`

### CSS
`button {`
`  border: 0;`
`  background: #0087cc;`
`  border-radius: 4px;`
`  box-shadow: 0 5px 0 #006599;`
`  color: #fff;`
`  cursor: pointer;`
`  font: inherit;`
`  margin: 0;`
`  outline: 0;`
`  padding: 12px 20px;`
`  transition: all .1s linear;`
`}`
`button:active {`
`  box-shadow: 0 2px 0 #006599;`
`  transform: translateY(3px);`
`}`






