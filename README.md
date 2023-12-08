
# CSS

This repo is all about my learning journey of CSS for front end web development.




## Authors

- [@adityahongal](https://www.github.com/adityahongal)


## 🔗 Links

[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/adityahongal/)



## 🚀 About Me
I'm a frontend web developer


## Roadmap

1. **CSS First Steps:**
   - Learning the basics of CSS syntax.
   - Understanding how CSS works with HTML.
   - Explore styling options like font, color, size, and spacing.

2. **CSS Building Blocks:**
   - Dive deeper into CSS with concepts like cascade and inheritance.
   - Explore various selector types and units.
   - Learn to style backgrounds, borders, and debug effectively.

3. **CSS Styling Text:**
   - Focus on styling text using CSS.
   - Cover fundamentals like font settings, boldness, italics, and spacing.
   - Explore advanced features like drop shadows, custom fonts, and styling lists/links.

4. **CSS Layout:**
   - Understand how to position elements in relation to the viewport and each other.
   - Explore different display settings and layout tools such as flexbox and CSS grid.
   - Learn positioning techniques, including modern and legacy approaches.




# Documentation

### 👷 What is CSS ?

In the HTML introduction, we learned that HTML structures documents for web browsers. By default, browsers apply basic styles like larger headings and spaced paragraphs to make content readable. These are default styles for basic legibility. But, to make websites visually appealing, we use CSS. CSS lets us control the look of HTML elements, allowing for unique designs instead of sticking to the browser's basic styles.

### 👷 What is CSS for ?

CSS is a language used to style and format documents for users. These documents, often structured with markup languages like HTML, are presented visually by browsers such as Firefox, Chrome, or Edge on screens, projectors, or printers. CSS serves various purposes, from basic text styling (changing colors and sizes of headings and links) to creating layouts, like organizing content into main areas and sidebars. Additionally, CSS can be used for effects like animation, enhancing the overall visual appeal of web documents.

### 👷 CSS syntax

CSS is a rule-based language where you define styles for specific elements on your webpage. A rule consists of a selector (identifying the HTML element), followed by declarations within curly braces. Declarations include property-value pairs, like setting the color and font size.

Example:
```css
h1 {
  color: red;
  font-size: 5em;
}
```
- In the above example, the CSS rule opens with a selector. This selects the HTML element that we are going to style. In this case, we are styling level one headings (`h1`).

- We then have a set of curly braces `{ }`.

- Inside the braces will be one or more declarations, which take the form of property and value pairs. We specify the property (`color` in the above example) before the colon, and we specify the value of the property after the colon (`red` in this example).

- This example contains two declarations, one for `color` and the other for `font-size`. Each pair specifies a property of the element(s) we are selecting (`h1` in this case), then a value that we'd like to give the property.

- CSS properties have different allowable values, depending on which property is being specified. In our example, we have the `color `property, which can take various color values. We also have the `font-size` property. This property can take various size units as a value.

### 👷 CSS modules

A CSS module is a self-contained section or unit of CSS that focuses on a specific aspect of styling or layout. It helps organize and manage styles for a website or web application, making the code more modular and maintainable.

For example, let's consider a simple website with a header, a main content area, and a footer. You can create separate CSS modules for each of these components to keep the styles organized.


## Getting Started with CSS

### 🥠 Adding CSS to our document

To apply CSS to an HTML document, the common and useful method is linking a separate CSS file. Follow these steps:

1. Create a file named `styles.css` in the same folder as your HTML document.
2. Link `styles.css` to your HTML document by adding the following line inside the `<head>`:


```html
<link rel="stylesheet" href="styles.css" />
```

This `<link>` element informs the browser about the stylesheet (using the `rel` attribute) and its location (specified in the `href` attribute).

3. Test the CSS by adding a rule to `styles.css`. For example:

```css
h1 {
  color: red;
}
```

4. Save both HTML and CSS files, then reload the page in a web browser. The level one heading should now appear in red.

### 🥠 Styling HTML elements

By making our heading red, we have already demonstrated that we can target and style an HTML element. We do this by targeting an element selector — this is a selector that directly matches an HTML element name. To target all paragraphs in the document, you would use the selector `p`. To turn all paragraphs green, you would use:

```css
p {
  color: green;
}
```

To target multiple selectors simultaneously, separate them with a comma. If you want both paragraphs and list items to be green, your rule would look like this:

```css
p,
li {
  color: green;
}
```

This CSS rule applies the green color to both paragraphs (`p`) and list items (`li`). This way, you can efficiently style multiple elements with similar properties.

### 🥠 Changing the default behavior of elements

When browsers render well-marked HTML documents, they apply default styles for readability. Headings are typically large and bold, and lists have bullets. These defaults are part of the browser's internal stylesheets, ensuring basic legibility.

However, you might desire a different style than the browser's default. In such cases, you can choose the HTML element you want to change and use a CSS rule to alter its appearance. For example, to remove bullets from an unordered list (`<ul>`), you can use the following CSS rule:

```css
li {
  list-style-type: none;
}
```

This CSS rule targets list items (`li`) and sets the `list-style-type` property to `none`, effectively removing the bullets. It demonstrates how CSS allows you to customize the visual presentation of HTML elements beyond the default browser styles.

### 🥠 Adding a Class

So far, we've styled elements based on their HTML element names, which affects all elements of that type in the document. To style a specific subset without changing others, you can add a class to the HTML element and target that class in your CSS.

1. Add a class attribute to the second list item in your HTML document:
   
   ```html
   <ul>
     <li>Item one</li>
     <li class="special">Item two</li>
     <li>Item <em>three</em></li>
   </ul>
   ```

2. Target the class "special" in your CSS file using a period (.):

   ```css
   .special {
     color: orange;
     font-weight: bold;
   }
   ```

   Save and refresh the page to see the result.

Now, any element with the class "special" will have the same appearance. For instance, you can apply the class to a `<span>` in a paragraph to make it orange and bold.

Sometimes, you might encounter rules with a selector that combines the HTML element selector and the class:

```css
li.special {
  color: orange;
  font-weight: bold;
}
```

This syntax means "target any `li` element that has a class of `special." If you use this, you can only apply the class to an `<li>` element, not a `<span>` or another element.

### 🥠 Styling things based on location

To style elements differently based on their location in the document, you can use selectors. Let's explore two of them: the descendant combinator and the next-sibling combinator.

1. **Descendant Combinator:**
To select an `<em>` that is nested inside an `<li>`, use the descendant combinator (a space between selectors):

   ```css
   li em {
     color: rebeccapurple;
   }
   ```

This selects any `<em>` element inside an `<li>`. In your example, the `<em>` in the third list item should turn purple, but the one inside the paragraph remains unchanged.

2. **Next-sibling Combinator:**
   To style a paragraph that directly follows a heading at the same hierarchy level, use the next-sibling combinator (`+`):

   ```css
   h1 + p {
     font-size: 200%;
   }
   ```

This rule selects a `<p>` element that is a direct sibling and comes immediately after an `<h1>`. Try adding this rule to your stylesheet.

**Example**

![Alt stylelocation](https://github.com/adityahongal/css/blob/main/images/styling%20things%20based%20on%20location.png)


### 🥠 Styling things based on state

The ability to style elements based on their state is an essential aspect of CSS. A common example of this is styling links, which have different states like unvisited, visited, hovered, focused, or active. CSS allows you to target and style these states differently.

For instance, you can style unvisited links in pink and visited links in green with the following CSS:

```css
a:link {
  color: pink;
}

a:visited {
  color: green;
}
```

In this example, `a:link` targets unvisited links, and `a:visited` targets visited links.

You can further modify the link's appearance when the user hovers over it, for example, by removing the underline:

```css
a:hover {
  text-decoration: none;
}
```

This CSS rule removes the underline when the user hovers over a link. These state-based styles provide interactive and dynamic visual feedback to users.

**Example**

![Alt stylestate](https://github.com/adityahongal/css/blob/main/images/styling%20element%20based%20on%20state.png)

### 🥠 Combining Selectors and Combinators

It's essential to understand that you can combine multiple selectors and combinators in CSS, creating more specific rules. For instance:

```css
/* Selects any <span> inside a <p> inside an <article> */
article p span {
}

/* Selects any <p> directly after a <ul> directly after an <h1> */
h1 + ul + p {
}
```

You can also combine different types together. Try adding the following to your code:

```css
body h1 + p .special {
  color: yellow;
  background-color: black;
  padding: 5px;
}
```

This rule styles any element with a class of `special` that is inside a `<p>`, which comes directly after an `<h1>`, which is inside the `<body>`. Combining selectors and combinators provides a powerful way to precisely target and style specific elements in your HTML structure.
## How CSS is structured ?

### 🧃 Applying CSS to HTML

There are three methods of applying CSS to a document: with an external stylesheet, with an internal stylesheet, and with inline styles.

#### External stylesheet

Using an external stylesheet, where CSS is in a separate file with a .css extension, is a common and efficient way to apply styling to a document. This method allows you to link a single CSS file to multiple web pages, ensuring consistent styling across all of them.

To reference an external CSS stylesheet in your HTML document, use the `<link>` element in the `<head>` section:

```html
<!doctype html>
<html lang="en-GB">
  <head>
    <meta charset="utf-8" />
    <title>My CSS experiment</title>
    <link rel="stylesheet" href="styles.css" />
  </head>
  <body>
    <h1>Hello World!</h1>
    <p>This is my first CSS example</p>
  </body>
</html>
```

The corresponding CSS file (`styles.css`) might look like this:

```css
h1 {
  color: blue;
  background-color: yellow;
  border: 1px solid black;
}

p {
  color: red;
}
```

The `href` attribute of the `<link>` element should reference the file on your file system where the CSS is stored. This method makes it easy to manage styles across multiple pages while keeping the CSS code separate from the HTML.

### Internal stylesheet

An internal stylesheet is CSS placed directly within an HTML document, enclosed in a `<style>` element within the `<head>` section. While it can be useful in specific situations, it becomes less efficient for sites with multiple pages.

Here's a simplified example:

```html
<!doctype html>
<html lang="en-GB">
  <head>
    <meta charset="utf-8" />
    <title>My CSS experiment</title>
    <style>
      h1 {
        color: blue;
        background-color: yellow;
        border: 1px solid black;
      }

      p {
        color: red;
      }
    </style>
  </head>
  <body>
    <h1>Hello World!</h1>
    <p>This is my first CSS example</p>
  </body>
</html>
```

Internal stylesheets can be useful in scenarios where modifying external CSS files is restricted, such as within certain content management systems. However, for sites with multiple pages, using internal stylesheets becomes less efficient. To apply consistent styling across multiple pages, you would need to include the internal stylesheet in each page, potentially leading to maintenance challenges as simple styling changes may require edits to numerous pages.

#### Inline styles

Inline styles are CSS declarations applied to a single HTML element using the `style` attribute. While you may encounter them in certain situations, it's generally considered a less efficient and less maintainable way to apply styles.

Here's a simplified example:

```html
<!doctype html>
<html lang="en-GB">
  <head>
    <meta charset="utf-8" />
    <title>My CSS experiment</title>
  </head>
  <body>
    <h1 style="color: blue; background-color: yellow; border: 1px solid black;">
      Hello World!
    </h1>
    <p style="color: red;">This is my first CSS example</p>
  </body>
</html>
```

Avoid using inline styles whenever possible. They are less efficient for maintenance because a single styling change may require multiple edits within a single web page. Additionally, inline styles mix presentational code with HTML and content, making the code harder to read and understand. Keeping code and content separate facilitates easier maintenance.

Inline styles are more common in restricted working environments, such as when a content management system (CMS) limits access to HTML body editing. You may also encounter inline styles in HTML emails to ensure compatibility with various email clients.

### 🧃 Selectors

Selectors in CSS target HTML elements to apply styles. If you're experiencing issues with styles not being applied as expected, the problem might lie in the selector not matching the elements as intended.

Here are some examples of valid selectors or lists of selectors:

```css
h1
a:link
.manythings
#onething
*
.box p
.box p:first-child
h1, h2, .intro
```

- `h1`: Targets all `<h1>` elements.
- `a:link`: Targets unvisited links.
- `.manythings`: Targets elements with the class "manythings."
- `#onething`: Targets the element with the ID "onething."
- `*`: Targets all elements.
- `.box p`: Targets paragraphs inside elements with the class "box."
- `.box p:first-child`: Targets the first paragraph inside elements with the class "box."
- `h1, h2, .intro`: Targets `<h1>` and `<h2>` elements, as well as elements with the class "intro."

Understanding and using selectors correctly is crucial for applying styles to the desired HTML elements.

### 🧃 Cascade and Specificity

In CSS, when two selectors target the same HTML element and have conflicting styles, the rules of cascade and specificity determine which style prevails. Consider the example below:

```css
.special {
  color: red;
}

p {
  color: blue;
}
```

In the HTML document:

```html
<p class="special">What color am I?</p>
```

Here, the class selector `.special` and the element selector `p` both apply styles to the paragraph. The class selector prevails, rendering the text red. The cascade rule dictates that conflicting styles are replaced by styles appearing later in the stylesheet.

However, if the styles for `p` were defined as follows:

```css
p {
  color: red;
}

p {
  color: blue;
}
```

The paragraph text would be blue because the later declaration replaces the conflicting earlier one.

Understanding specificity is crucial. In cases where a class and an element selector conflict, the class is more specific and takes precedence. Experimenting with your own HTML and CSS can help reinforce these concepts. Remember, recognizing potential conflicts and understanding specificity are vital for resolving styling issues in CSS.

### 🧃 Properties and Values

CSS, at its core, comprises two essential components:

1. **Properties:** Human-readable identifiers that specify which stylistic features to modify. Examples include font-size, width, and background-color.

2. **Values:** Each property is assigned a value, indicating how to style the specified feature.

A CSS declaration consists of a property-value pair. For instance, in the declaration `color: blue`, "color" is the property, and "blue" is the value.

Declarations are organized within CSS Declaration Blocks. A block contains one or more declarations, enclosed in curly braces.

CSS rulesets (or rules) are formed by pairing declaration blocks with selectors. A rule defines how styling should be applied to specific elements. For example, the rule for `h1` might set the color property to blue.

CSS properties and values are case-insensitive. The property and value are separated by a colon (:).

Note: If a property or value is unknown or invalid, the declaration is ignored by the browser's CSS engine.

Note: In CSS, US spelling is the standard. For example, "color" is used instead of "colour" for consistency and compatibility.

### 🧃 Functions

In CSS, some values take the form of functions, and one example is the `calc()` function. This function allows for simple math within CSS, as demonstrated below:

HTML:
```html
<div class="outer"><div class="box">The inner box is 90% - 30px.</div></div>
```

CSS:
```css
.outer {
  border: 5px solid black;
}

.box {
  padding: 10px;
  width: calc(90% - 30px);
  background-color: rebeccapurple;
  color: white;
}
```

The `calc()` function, in this case, calculates the width of the inner box to be 90% of the containing block width, minus 30 pixels. This dynamic calculation allows for flexibility in responsive designs.

**The Rendered example looks like**

![Alt calcfunction](https://github.com/adityahongal/css/blob/main/images/calc%20function%20in%20CSS.png)


### 🧃 Transform functions

In CSS, functions are also used for certain values, such as in the case of the `transform` property with the `rotate()` function. Here's an example:

HTML:
```html
<div class="box"></div>
```

CSS:
```css
.box {
  margin: 30px;
  width: 200px;
  height: 200px;
  background-color: rebeccapurple;
  transform: rotate(0.8turn);
}
```

In this example, the `rotate()` function is applied to the `transform` property, causing the `.box` element to rotate by 0.8 turns. Functions like these provide a powerful way to manipulate and animate elements in CSS.

**Example looks like**

![Alt transformfunction](https://github.com/adityahongal/css/blob/main/images/transform%20function%20in%20css.png)

### 🧃 @rules

CSS @rules, pronounced "at-rules," provide instructions for how CSS should behave or perform certain actions. One common @rule is @import, which is used to import another stylesheet into the current CSS file:

```css
@import "styles2.css";
```

Another frequently used @rule is @media, which is employed to create media queries. Media queries enable the application of conditional styling based on certain conditions, such as the size of the browser viewport. In the example below, the default background color for the `<body>` element is set to pink. However, a media query is used to apply a blue background if the viewport is wider than 30em:

```css
body {
  background-color: pink;
}

@media (min-width: 30em) {
  body {
    background-color: blue;
  }
}
```

This example demonstrates how @media is utilized to create a responsive design, changing the background color based on the width of the viewport.

### 🧃 Shorthands

In CSS, certain properties, such as font, background, padding, border, and margin, are referred to as shorthand properties. Shorthand properties allow you to set multiple values in a single line, simplifying the code.

For instance, the following line of code using the `padding` shorthand property:

```css
padding: 10px 15px 15px 5px;
```

is equivalent to these four lines of code:

```css
padding-top: 10px;
padding-right: 15px;
padding-bottom: 15px;
padding-left: 5px;
```

Similarly, the following line using the `background` shorthand property:

```css
background: red url(bg-graphic.png) 10px 10px repeat-x fixed;
```

is equivalent to these five lines:

```css
background-color: red;
background-image: url(bg-graphic.png);
background-position: 10px 10px;
background-repeat: repeat-x;
background-attachment: fixed;
```

These shorthand properties provide a more concise way to express multiple values for a set of related properties.In CSS, certain properties, such as font, background, padding, border, and margin, are referred to as shorthand properties. Shorthand properties allow you to set multiple values in a single line, simplifying the code.

For instance, the following line of code using the `padding` shorthand property:

```css
padding: 10px 15px 15px 5px;
```

is equivalent to these four lines of code:

```css
padding-top: 10px;
padding-right: 15px;
padding-bottom: 15px;
padding-left: 5px;
```

Similarly, the following line using the `background` shorthand property:

```css
background: red url(bg-graphic.png) 10px 10px repeat-x fixed;
```

is equivalent to these five lines:

```css
background-color: red;
background-image: url(bg-graphic.png);
background-position: 10px 10px;
background-repeat: repeat-x;
background-attachment: fixed;
```

These shorthand properties provide a more concise way to express multiple values for a set of related properties.

### 🧃 Whitespaces

In CSS, white space refers to actual spaces, tabs, and new lines. Similar to how browsers ignore white space in HTML, they also disregard white space inside CSS. While white space itself doesn't affect the styling, its value lies in improving readability.

For instance, the following declarations are valid CSS:

```css
margin: 0 auto;
padding-left: 10px;
```

However, the following declarations are invalid due to spacing errors:

```css
margin: 0auto;
padding- left: 10px;
```

In the first example, `0auto` is not recognized as a valid value for the `margin` property, as it should be two separate values: `0` and `auto`. In the second example, the browser doesn't recognize `padding-` as a valid property because of the space issue. It should be `padding-left` without any spaces.

To ensure correctness, always separate distinct values with at least one space and keep property names and values together as single, unbroken strings.


## How CSS works ?

#### 💮 How does CSS actually work ?

When a browser displays a webpage, it undergoes a series of stages:

1. **Loading HTML:** The browser fetches the HTML content, often from the network.

2. **Creating the DOM:** The browser converts the HTML into a DOM (Document Object Model), representing the document in the computer's memory.

3. **Fetching Resources:** The browser fetches additional resources linked in the HTML, such as images and linked CSS. JavaScript is handled separately.

4. **Parsing CSS:** The browser parses the fetched CSS, organizing rules into different categories based on selectors (e.g., element, class, ID).

5. **Building the Render Tree:** A render tree is created by associating styles with corresponding nodes in the DOM, forming the structure of the visual representation (render tree).

6. **Layout:** The render tree is arranged in the intended structure after applying styles.

7. **Painting:** The final visual display of the page is shown on the screen.

This simplified overview outlines the major steps browsers take to render a webpage. Note that different browsers may handle these steps in varying ways.


![Alt CSS works](https://developer.mozilla.org/en-US/docs/Learn/CSS/First_steps/How_CSS_works/rendering.svg)


#### 💮 Above the DOM

The DOM (Document Object Model) has a tree-like structure where each element, attribute, and text in the markup language becomes a node in the tree. Nodes are characterized by their relationships with other nodes, with some elements acting as parents to child nodes, and child nodes having siblings.

Understanding the DOM is crucial for designing, debugging, and maintaining CSS. The DOM serves as the meeting point for your CSS and the document's content. When using browser DevTools, you navigate the DOM to select items and inspect applied rules. This understanding facilitates effective interaction with the DOM to analyze and manipulate the document's structure and styling.

#### 💮 A real DOM representation

Instead of a lengthy explanation, let's examine an example to understand how a real HTML snippet is transformed into a DOM.

Consider the following HTML code:

```html
<p>
  Let's use:
  <span>Cascading</span>
  <span>Style</span>
  <span>Sheets</span>
</p>
```

In the DOM, the node corresponding to the `<p>` element is a parent. Its children include a text node and three nodes corresponding to the `<span>` elements. The `<span>` nodes are also parents with text nodes as their children:

```
P
├─ "Let's use:"
├─ SPAN
|  └─ "Cascading"
├─ SPAN
|  └─ "Style"
└─ SPAN
    └─ "Sheets"
```

This representation illustrates how a browser interprets the HTML snippet, rendering the DOM tree and then displaying it in the browser accordingly.

#### 💮 Applying CSS to the DOM

Let's imagine we add some CSS to our document to style it. The original HTML is as follows:

```html
<p>
  Let's use:
  <span>Cascading</span>
  <span>Style</span>
  <span>Sheets</span>
</p>
```

Suppose we apply the following CSS to it:

```css
span {
  border: 1px solid black;
  background-color: lime;
}
```

The browser parses the HTML and creates a DOM from it. Next, it parses the CSS. Since the only rule available in the CSS has a `span` selector, the browser quickly applies that rule to each one of the three `<span>` elements. Finally, it paints the final visual representation on the screen.

The updated output shows the styled `<span>` elements with a black border and lime background.

#### output

![Alt CSStoDOM](https://github.com/adityahongal/css/blob/main/images/applying%20css%20to%20dom.png)


#### 💮 What happens if a browser encounters CSS it doesn't understand?

If a browser encounters a CSS selector or declaration it doesn't recognize, it simply ignores it and moves on to the next part of the CSS. This behavior is useful for handling cases where there might be misspellings, errors, or new features not supported by certain browsers.

For example, in the following code, the British English spelling "colour" is used, which is incorrect. As a result, the color property is not recognized, but the other CSS rules are applied:

```html
<p>I want this text to be large, bold and blue.</p>
```

```css
p {
  font-weight: bold;
  colour: blue; /* incorrect spelling of the color property */
  font-size: 200%;
}
```

This behavior allows for graceful degradation, where new or unsupported CSS features can be used as enhancements without causing errors. For instance, if a browser doesn't support the calc() function, a fallback value in pixels can be provided, ensuring that older browsers use the fallback while newer ones interpret and apply the calc() value:

```css
.box {
  width: 500px;
  width: calc(100% - 50px);
}
```


## Simple Biography Page

![Alt biopage](https://github.com/adityahongal/css/blob/main/images/simple%20biography%20page.png)


