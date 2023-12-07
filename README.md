
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


