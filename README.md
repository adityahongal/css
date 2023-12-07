
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



