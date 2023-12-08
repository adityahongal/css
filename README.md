
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



## CSS building blocks

### 🏗️ CSS selectors

In CSS, selectors are used to target the HTML elements on our web pages that we want to style. There are a wide variety of CSS selectors available, allowing for fine-grained precision when selecting elements to style.

#### What is a Selector ?

A CSS selector is a pattern that identifies which HTML elements should have specific styles applied to them. It specifies the target elements for a CSS rule. These selectors can vary, ranging from simple elements like `h1` to more specific targets like `.special` for a class. The selected elements are referred to as the subject of the selector.

####  Selector lists

When you have multiple elements or classes that should have the same CSS styles, you can combine them into a selector list. This allows you to apply the same rule to multiple selectors simultaneously. For instance, if you want both `h1` and the class `.special` to have the color blue, you can write separate rules or combine them into a selector list:

Separate rules:

```css
h1 {
  color: blue;
}

.special {
  color: blue;
}
```

Combined into a selector list:

```css
h1, .special {
  color: blue;
}
```

You can include white space before or after the comma for readability, and you may choose to put each selector on a new line for better organization:

```css
h1,
.special {
  color: blue;
}
```

Keep in mind that if there's an invalid selector in the list, the entire rule will be ignored. For example, if you mistakenly write `..special` instead of `.special`, the entire rule will be deemed invalid:

```css
h1, ..special {
  color: blue;
}
```

In this case, neither the `h1` nor the `.special` will be styled because of the invalid selector.

### Types of selectors

Selectors in CSS can be categorized into different groups, each serving a specific purpose. Here are a few key groups:

1. **Type, Class, and ID Selectors:**
   - **Type Selector:** Targets HTML elements based on their type (e.g., `h1`, `p`).
     ```css
     h1 {
       /* Styles for h1 elements */
     }
     ```

   - **Class Selector:** Targets elements with a specific class attribute value.
     ```css
     .box {
       /* Styles for elements with class="box" */
     }
     ```

   - **ID Selector:** Targets elements with a specific ID attribute value.
     ```css
     #unique {
       /* Styles for elements with id="unique" */
     }
     ```

2. **Attribute Selectors:**
   - Targets elements based on the presence or value of their attributes.
     ```css
     a[title] {
       /* Styles for anchor elements with a title attribute */
     }

     a[href="https://example.com"] {
       /* Styles for anchor elements with an href attribute equal to "https://example.com" */
     }
     ```

3. **Pseudo-classes and Pseudo-elements:**
   - **Pseudo-classes:** Selects elements based on certain states or conditions (e.g., `:hover` for hovered elements).
     ```css
     a:hover {
       /* Styles for hovered anchor elements */
     }
     ```

   - **Pseudo-elements:** Selects a specific part of an element (e.g., `::first-line` for the first line of text in a block).
     ```css
     p::first-line {
       /* Styles for the first line of text in a paragraph */
     }
     ```

4. **Combinators:**
   - Combines multiple selectors to target specific elements or relationships between elements (e.g., descendant combinator, child combinator).
     ```css
     article > p {
       /* Styles for paragraphs that are direct children of article elements */
     }
     ```

Understanding these groups of selectors provides a powerful toolkit for styling HTML documents with CSS.

### 🏗️ Universal selectors

The universal selector in CSS, denoted by an asterisk (*), selects all elements in a document or within a specific parent element when combined with other selectors and a descendant combinator.

One common use case is in "reset stylesheets," where it helps remove default browser styling. The universal selector is employed selectively for specific situations where global changes are needed.

Here's a simple example of using the universal selector in a CSS reset stylesheet:

```css
/* Reset styles to remove default browser styling */

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  /* Add other reset styles as needed */
}

/* Your additional styles go here */
body {
  font-family: 'Arial', sans-serif;
  background-color: #f0f0f0;
}
```

In this example, the universal selector (`*`) is used to set `margin`, `padding`, and `box-sizing` to create a consistent starting point for styling. These styles are then overridden or extended as needed for specific elements in the document.

#### Using the universal selector to make your selectors easier to read

The universal selector can enhance readability in certain situations.

```css
/* Original selector without universal selector */
article :first-child {
  font-weight: bold;
}

/* Improved readability with universal selector */
article *:first-child {
  font-weight: bold;
}
```

In the improved version, the universal selector (`*`) makes it clearer that we are targeting any element that is the first child of an `<article>` element or the first child of any descendant element within an `<article>`. This helps avoid confusion with similar selectors and enhances code readability.

### 🏗️ Class selector in detail

The case-sensitive class selector starts with a dot (.) character. It will select everything in the document with that class applied to it.


```css
/* Selects everything with the specified class */
.highlight {
  /* Styles for elements with the "highlight" class */
}

/* Targeting specific elements with the class */
h1.highlight {
  /* Styles for <h1> elements with the "highlight" class */
}

span.highlight {
  /* Styles for <span> elements with the "highlight" class */
}

/* Targeting an element with multiple classes applied */
.element1.element2 {
  /* Styles for elements with both "element1" and "element2" classes */
}
```

In the simplified version, the class selector is used to select everything with the specified class. Additionally, specific elements with the class are targeted using the type selector (e.g., `h1`, `span`). The example also demonstrates how to target an element with multiple classes applied, ensuring that the styles are applied only when both classes are present.

### 🏗️ Attribute Selectors

Elements can have attributes that give further detail about the element being marked up. In CSS you can use attribute selectors to target elements with certain attributes. This lesson will show you how to use these very useful selectors.

#### Presence and Value selectors

These selectors enable the selection of an element based on the presence of an attribute alone (e.g., href) or various matches against the value of the attribute.


| Selector            | Example                               | Description                                                                                                       |
|---------------------|---------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| `[attr]`            | `a[title]`                            | Matches elements with an `attr` attribute (whose name is the value in square brackets).                           |
| `[attr=value]`      | `a[href="https://example.com"]`       | Matches elements with an `attr` attribute whose value is exactly `value` — the string inside the quotes.           |
| `[attr~=value]`     | `p[class~="special"]`                  | Matches elements with an `attr` attribute whose value is exactly `value` or contains `value` in its list of values. |
| `[attr\|=value]`    | `div[lang\|="zh"]`                    | Matches elements with an `attr` attribute whose value is exactly `value` or begins with `value` followed by a hyphen. |

#### Substring matching selectors

These selectors provide advanced matching options for substrings within attribute values. For instance, if you have classes like box-warning and box-error and want to select elements whose class attribute starts with the string "box-", you can use [class^="box-"] to match both (similar to [class|="box"] described earlier).

This enables more flexible and precise attribute value matching.


```markdown
| Selector        | Example              | Description                                                    |
| --------------- | -------------------- | -------------------------------------------------------------- |
| [attr^=value]   | li[class^="box-"]    | Matches elements with an attr attribute, beginning with value.  |
| [attr$=value]   | li[class$="-box"]    | Matches elements with an attr attribute, ending with value.     |
| [attr*=value]   | li[class*="box"]     | Matches elements with an attr attribute, containing value.      |
```

This table provides a concise overview of the attribute selectors along with examples and their corresponding descriptions.

### 🏗️ Case sensitivity

To perform case-insensitive matching for attribute values, add the `i` flag before the closing bracket. This flag instructs the browser to match ASCII characters case-insensitively. Without the flag, the matching is done based on the case-sensitivity of the document language, which is case-sensitive in HTML.

For example:

- `a[title="example" i]` matches elements with a title attribute, case-insensitively equal to "example".
- `input[type="text" i]` matches input elements with a type attribute, case-insensitively equal to "text".

This approach ensures that the attribute values are matched without considering case sensitivity.


### 🏗️ Pseudo classes and Pseudo elements

#### Pseudo classes

A pseudo-class is a selector that selects elements that are in a specific state, e.g. they are the first element of their type, or they are being hovered over by the mouse pointer. They tend to act as if you had applied a class to some part of your document, often helping you cut down on excess classes in your markup, and giving you more flexible, maintainable code.

Pseudo-classes are keywords that start with a colon. For example, `:hover` is a pseudo-class.

For example instead of adding a class to the first paragraph, you can use the `:first-child` pseudo-class selector to style the first paragraph within an article. This approach avoids the need to add or modify classes in the HTML, providing a more flexible and maintenance-friendly solution:

CSS:

```css
article p:first-child {
  font-size: 120%;
  font-weight: bold;
}
```

HTML:

```html
<article>
  <p>Veggies es bonus vobis, proinde vos postulo essum magis kohlrabi welsh onion daikon amaranth tatsoi tomatillo
    melon azuki bean garlic.</p>

  <p>Gumbo beet greens corn soko endive gumbo gourd. Parsley shallot courgette tatsoi pea sprouts fava bean collard
    greens dandelion okra wakame tomato. Dandelion cucumber earthnut pea peanut soko zucchini.</p>
</article>
```

With this CSS rule, the first paragraph inside the `<article>` element will have a font size of 120% and a bold font weight, without the need for adding specific classes to paragraphs.

#### User-action pseudo classes

Some pseudo-classes only apply when the user interacts with the document in some way. These user-action pseudo-classes, sometimes referred to as dynamic pseudo-classes, act as if a class had been added to the element when the user interacts with it. Examples include:

- `:hover` — mentioned above; this only applies if the user moves their pointer over an element, typically a link.
- `:focus` — only applies if the user focuses the element by clicking or using keyboard controls.

### Pseudo elements

Pseudo-elements behave in a similar way. However, they act as if you had added a whole new HTML element into the markup, rather than applying a class to existing elements.

Pseudo-elements start with a double colon `::`. `::before` is an example of a pseudo-element.

For example `::first-line` pseudo-element selector allows you to style the first line of a block-level element. Here's an example:

```css
/* ::first-line pseudo-element */
article p::first-line {
  font-size: 120%;
  font-weight: bold;
}
```

In this example, the first line of each paragraph (`<p>`) inside an `<article>` element will have an increased font size and bold font weight.

This is a convenient way to style specific parts of text without the need for additional HTML elements or classes. The `::first-line` pseudo-element automatically selects the first line, making it adaptable to changes in content or layout.

#### Combining pseudo-classes and pseudo-elements

If you wanted to make the first line of the first paragraph bold you could chain the `:first-child` and `::first-line` selectors together. Try editing the previous live example so it uses the following CSS. We are saying that we want to select the first line, of the first `<p>` element, which is inside an `<article>` element.

```css
/* ::first-line pseudo-element of the first paragraph inside an article */
article p:first-child::first-line {
  font-size: 120%;
  font-weight: bold;
}
```

#### Generating content with ::before and ::after

The `::before` and `::after` pseudo-elements are used to generate content before and after an element's actual content, respectively. They are often used to add decorative elements or additional information without altering the HTML markup.

Here's a simple example of how to use `::before` and `::after` to add quotes to a blockquote:

```css
/* Add quotes before and after the content of blockquote */
blockquote::before {
  content: "\201C"; /* Unicode character for left double quotation mark */
}

blockquote::after {
  content: "\201D"; /* Unicode character for right double quotation mark */
}
```

And here's the corresponding HTML:

```html
<blockquote>
  This is a quote.
</blockquote>
```

In this example, the `::before` pseudo-element adds an opening double quotation mark before the content of the `blockquote`, and the `::after` pseudo-element adds a closing double quotation mark after the content.

You can use the `content` property to specify what content should be generated. It can be text, an image, or other CSS properties. Keep in mind that the `content` property is mandatory for `::before` and `::after` pseudo-elements to generate content.

### 🏗️ Combinators

#### Descendant combinator

The descendant combinator — typically represented by a single space (" ") character — combines two selectors such that elements matched by the second selector are selected if they have an ancestor (parent, parent's parent, parent's parent's parent, etc.) element matching the first selector. Selectors that utilize a descendant combinator are called descendant selectors.

```html
body article p
```

#### Child combinator

The child combinator (`>`) is placed between two CSS selectors. It matches only those elements matched by the second selector that are the direct children of elements matched by the first. Descendant elements further down the hierarchy don't match. For example, to select only `<p>` elements that are direct children of `<article>` elements:

```html
article > p
```

#### Next-sibling combinator

The next-sibling combinator (`+`) is placed between two CSS selectors. It matches only those elements matched by the second selector that are the next sibling element of the first selector. For example, to select all `<img>` elements that are immediately preceded by a `<p>` element:

```html
p + img
```

#### Subsequent-sibling combinator

If you want to select siblings of an element even if they are not directly adjacent, then you can use the subsequent-sibling combinator (~). To select all <img> elements that come anywhere after <p> elements, we'd do this:

```html
p ~ img
```

#### Creating complex selectors with nesting

The CSS nesting module simplifies the way nested rules with combinators are written. Here's a breakdown of the examples you provided:

1. Using the general sibling combinator (`~`):

```css
p {
  ~ img {
    /* Styles for img elements that are siblings of p elements */
  }
}
```

This is equivalent to the following standard CSS:

```css
p ~ img {
  /* Styles for img elements that are siblings of p elements */
}
```

2. Using the `&` nesting selector:

```css
p {
  & img {
    /* Styles for img elements that are descendants of p elements */
  }
}
```

This is equivalent to the following standard CSS:

```css
p img {
  /* Styles for img elements that are descendants of p elements */
}
```

In both cases, the nesting module simplifies the syntax for writing nested rules with combinators. It makes the CSS more readable and reflects the hierarchical relationship between elements in a more natural way.

#### Using combinators

You can use combinators to refine your selectors and target specific elements within your document. For instance, to select list items with a class of "a" that are direct children of a `<ul>`, you can use the following CSS:

```css
ul > li[class="a"] {
  /* Styles for list items with class "a" that are direct children of a <ul> */
}
```

However, be cautious when creating complex selectors that are very specific to the document structure. This can make it challenging to reuse the CSS rules in other contexts. It is generally advisable to create simple classes and apply them to elements, providing more flexibility and maintainability. The knowledge of combinators becomes particularly useful when styling elements in situations where you cannot modify the HTML directly, such as with content generated by a CMS.


### 🏗️ Cascade, specificity, and inheritance

#### Conflicting rules

CSS, or Cascading Style Sheets, is a crucial aspect of web development. The term "cascading" holds great significance as it refers to the way styles are applied, and understanding this behavior is essential in CSS.

When working on projects, you may encounter situations where the expected styles for an element are not taking effect. This often happens when conflicting rules are created, assigning different values to the same property for a particular element. The concepts of cascade and specificity come into play to determine which rule takes precedence in such conflicts. It's important to comprehend these mechanisms to identify and resolve styling issues accurately.

Another key concept is inheritance, where certain CSS properties inherit values from the parent element by default, while others do not. This behavior can lead to unexpected outcomes, and understanding inheritance is crucial for anticipating how styles propagate through the document.

#### Cascade

In CSS, stylesheets cascade, meaning that the origin, cascade layer, and order of CSS rules play a crucial role. When two rules from the same cascade layer have equal specificity and can apply to an element, the one defined last in the stylesheet takes precedence.

For instance, consider the following example where two rules could potentially apply to an `<h1>` element. In this case, the text inside the `<h1>` will be colored blue because both rules are from the same source, have an identical element selector, and thus, carry the same specificity. The winning rule is determined by the order in which they appear in the source, with the last one taking precedence.

```css
h1 {
  color: red;
}

h1 {
  color: blue;
}
```

In this example, the text color will be blue due to the second rule being defined last. Understanding the cascade order is crucial when dealing with conflicting styles in your CSS.

#### Specificity

Specificity is the mechanism that the browser employs to determine which property value should be applied to an element when there are conflicting styles. It's a measure of how specific a selector's selection is:

- Element selectors are less specific, as they target all elements of a particular type on a page.
- Class selectors, attribute selectors, and pseudo-classes have more specificity than element selectors.
- Pseudo-elements have the same specificity as regular element selectors.

Consider the following example with conflicting styles for an `<h1>` element. The text color ends up being red because the rule with the class selector `.main-heading` has higher specificity, outweighing the rule with the `<h1>` element selector, even though the latter appears later in the source order.

```css
.main-heading {
  color: red;
}

h1 {
  color: blue;
}
```

In this scenario, the text color will be red due to the higher specificity of the class selector. Understanding specificity is crucial when dealing with conflicting styles in your CSS.

#### Inheritance

Inheritance is a key concept in CSS, defining whether certain CSS property values set on parent elements are passed down to their child elements. However, not all properties are inherited.

For instance, if you set a color and font-family on a parent element, these styles will be inherited by its child elements, unless overridden with different values.

```css
body {
  color: blue;
}

span {
  color: black; /* Overrides the inherited color */
}
```

However, some properties do not inherit. For example, setting a width of 50% on an element does not automatically apply a width of 50% to its descendants. If this were the case, working with CSS would be much more challenging.

Understanding which properties inherit and which don't is crucial for effective CSS styling.

