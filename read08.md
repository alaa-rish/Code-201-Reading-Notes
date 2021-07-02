---
# More CSS Layout
---

## ***Layout position Property***

![lo](https://bs-uploads.toptal.io/blackfish-uploads/uploaded_file/file/197755/image-1583190798408-7af80aeb943477b9375814bc95245a4e.png)


The position property specifies the type of positioning method used for an element (static, relative, fixed, absolute or sticky).

There are five different position values:

+ static
+ relative
+ fixed
+ absolute
+ sticky

### 1. `position: static;`

HTML elements are positioned static by default.

Static positioned elements are not affected by the top, bottom, left, and right properties.

An element with position: static; is not positioned in any special way; it is always positioned according to the normal flow of the page.

### 2. `position: relative;`

An element with position: relative; is positioned relative to its normal position.

Setting the top, right, bottom, and left properties of a relatively-positioned element will cause it to be adjusted away from its normal position. Other content will not be adjusted to fit into any gap left by the element.

### 3. `position: fixed;`

An element with position: fixed; is positioned relative to the viewport, which means it always stays in the same place even if the page is scrolled. The top, right, bottom, and left properties are used to position the element.

A fixed element does not leave a gap in the page where it would normally have been located.

### 4. `position: absolute;`

An element with position: absolute; is positioned relative to the nearest positioned ancestor (instead of positioned relative to the viewport, like fixed).

However; if an absolute positioned element has no positioned ancestors, it uses the document body, and moves along with page scrolling.

### 5. `position: sticky;`

An element with position: sticky; is positioned based on the user's scroll position.

A sticky element toggles between relative and fixed, depending on the scroll position. It is positioned relative until a given offset position is met in the viewport - then it "sticks" in place (like position:fixed).