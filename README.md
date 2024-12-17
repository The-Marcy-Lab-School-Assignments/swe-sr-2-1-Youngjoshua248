# Technical Writing Assignment

For guidance on setting up and submitting this assignment, refer to the Marcy lab School Docs How-To guide for [Working with Short Response and Coding Assignments](https://marcylabschool.gitbook.io/marcy-lab-school-docs/fullstack-curriculum/how-tos/working-with-assignments#how-to-work-on-assignments).

## Prompt 1

Do some research on semantic and non-semantic elements and share your findings. Your response should include:

- Examples of semantic and non-semantic tags
- The differences between semantic and non-semantic tags
- The benefits of using semantic tags (when possible)

### Response 1

Semantic vs Non-Semantic Elements
Definition:

Semantic Tags: HTML tags that give meaning to their content, improving accessibility and SEO.
Non-Semantic Tags: Generic tags used mainly for layout and styling without conveying specific meaning.
Examples
Semantic Tags:

<header>, <footer>, <main>, <article>, <nav>, <section>, <aside>
Non-Semantic Tags:

<div>, <span>
Benefits of Semantic Tags
Accessibility: Easier for screen readers and assistive technologies to interpret.
SEO: Improves search engines' ability to index content.
Maintainability: Clear, meaningful structure leads to easier code management.
Standardization: Aligns with modern HTML5 standards.
Using semantic tags creates a better user and developer experience by enhancing meaning, accessibility, and clarity.

## Prompt 2

Do some research on accessibility. What are some ways to make your website more accessible? Explain why it is important for developers to create websites that meet accessibility standards.

### Response 2

Accessibility ensures that all users, including those with disabilities, can access and interact with your website effectively. Here are several ways to make a website more accessible:

Use Semantic HTML: Use semantic tags like <header>, <footer>, <nav>, and <main> to give structure and context to your content.
Add Alternative Text: Provide descriptive alt text for images to help visually impaired users who rely on screen readers.

Keyboard Navigation: Ensure that users can navigate your site entirely using a keyboard, without needing a mouse.
Color Contrast: Maintain sufficient contrast between text and background to ensure readability for users with visual impairments.

Responsive Design: Ensure your site works on all devices, including screen readers on mobile devices or different screen sizes.

Accessible Forms: Label form fields properly with <label> elements and ensure users can easily interact with form inputs.

Use ARIA Roles: Apply Accessible Rich Internet Applications (ARIA) roles to dynamic content that does not have native semantic HTML support.

Enable Text Resizing: Allow text to be resized without breaking the layout to support users with low vision.

Provide Clear Instructions: Clearly label navigation, buttons, and interactive elements to ensure they are easily understood.

Avoid Relying on Color Alone: Don’t rely solely on color to convey meaning, as colorblind users may struggle to interpret cues based only on color.

Why Accessibility Matters
Developers must prioritize accessibility to ensure inclusivity, allowing users with varying abilities, disabilities, or technology limitations to interact with their websites. An accessible site offers equitable experiences for everyone, helping to remove barriers for users with visual impairments, hearing impairments, motor difficulties, or cognitive disabilities. Moreover, websites that follow accessibility standards are more likely to be inclusive and appeal to a broader audience. Compliance with accessibility laws (e.g., the ADA in the U.S. or the WCAG guidelines globally) is not just ethical but often a legal requirement. Accessible websites also improve usability for all users by enhancing user experience through clear design choices, better navigation, and improved interface clarity. Furthermore, search engines reward accessible sites, improving SEO performance. Prioritizing accessibility demonstrates social responsibility and ensures all users can engage with the content without limitations.

## Prompt 3

It is possible to add "inline" CSS styles to our html elements using the `style` attribute like so:

```html
<p style="color: red;">hello world</p>
```

While this is possible, it is a best practice to instead write styles in a separate CSS file. Provide at least one argument for why it _might_ be considered useful to write inline styles, and then provide a more compelling argument for writing styles in a separate CSS file.

### Response 3

Argument for Inline Styles: Inline styles might be considered useful in situations where you need to apply a quick, one-time style change to a single element that won't be reused or require maintenance across multiple pages. For example, if a particular style is unique to a single element or only needed temporarily, using the style attribute can save time and eliminate unnecessary complexity.

Key Benefits:

Reusability: Write styles once and reuse them across multiple HTML pages.
Cleaner HTML: HTML code remains clean, readable, and easier to maintain.
Maintainability: Centralized style changes are easier. Update one CSS file, and the changes automatically apply everywhere, saving time and reducing errors.
Performance: Browsers cache external CSS files, improving load times for repeat visitors.
Team Collaboration: Separate CSS allows designers and developers to work independently on the HTML and style layers.

## Prompt 4

Imagine you are teaching a brand new programmer a brief lesson about the `class` and `id` attributes in HTML as well as how to use them to style elements using CSS. Your lesson should have the following components:

- An explanation of the concept of "classes" and "ids" with an analogy.
- An example of the usage using an HTML code block and a CSS code block.
- An explanation of the syntax using the terms: **attribute**, **selector**

### Response 4

Concept Explanation
When working with HTML and CSS, the class and id attributes help you target specific elements for styling. Think of them like names or labels that make it easier to identify and style elements on a webpage.

Analogy: Imagine you're organizing a group of students in a classroom.

Class: A "class" is like a group that multiple students can belong to. For example, all students in "Art Club" could be members of the same class. You can give all members of this group the same instruction or style.
ID: An "id" is like a unique name for one specific student. No two students can share the same unique name (id), just like IDs in HTML must always be unique across a page.
HTML and CSS Example
Let's see how class and id work in practice:

HTML Code:

<!DOCTYPE html>
<html>
<head>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <!-- Using a class for multiple elements -->
  <p class="highlight">This is a highlighted paragraph.</p>
  <p class="highlight">This is another highlighted paragraph.</p>

  <!-- Using an id for a single, unique element -->
  <p id="uniqueText">This is a uniquely styled paragraph.</p>
</body>
</html>
CSS Code (styles.css):

/_ Target elements with the 'highlight' class _/
.highlight {
color: blue;
font-weight: bold;
}

/_ Target the unique paragraph with the 'id' _/
#uniqueText {
color: red;
font-style: italic;
}
Explanation of the Syntax
Attribute:
In HTML, class and id are attributes that you can add to elements to give them a name or identifier.
Example:

<p class="highlight">...</p>
Here, class="highlight" assigns the class name "highlight" to this <p> element.
Selector:
In CSS, a selector is the pattern or name you use to target specific elements in your HTML for styling.
For a class, the selector uses a period (.) followed by the class name:
.highlight {
  color: blue;
}
For an id, the selector uses a hash (#) followed by the id name:
#uniqueText {
  color: red;
}

## Prompt 5

The Document Object Model (DOM) API provides functions for manipulating HTML documents. It is possible to build an entire website using only JavaScript and the DOM API, however is that the best practice?

When building a website, how can I decide which content I should write using HTML/CSS and which content I should create using the JavaScript and the DOM API?

### Response 5

While it is technically possible to build an entire website using just JavaScript and the DOM API by dynamically creating and manipulating elements, it is not considered best practice. Separating HTML/CSS for structure and style, and JavaScript for behavior, leads to better performance, maintainability, scalability, and accessibility.

When to Use HTML/CSS vs JavaScript with the DOM API
You can decide which content or structure to define using HTML/CSS and which to dynamically create or modify with JavaScript by considering their roles:

1. Use HTML/CSS for Static Content and Structure:

HTML and CSS are best suited for content and structure that do not change dynamically. They define the foundational elements of a webpage.

Examples of what should typically go in HTML/CSS:

Static content like headings, paragraphs, and images.
Layouts and fixed page structure (e.g., headers, footers, sidebars).
Styling, including color schemes, typography, spacing, and visual design.
Why? These are easier to maintain, faster to load, and ensure better accessibility (screen readers and assistive technologies depend on properly written semantic HTML).

Example:

<!DOCTYPE html>
<html>
<head>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <header>
    <h1>Welcome to My Website</h1>
  </header>
  <main>
    <p>This is static content defined with HTML.</p>
  </main>
</body>
</html>
/* Static visual styles */
header {
  background-color: lightblue;
  padding: 10px;
  text-align: center;
}
2. Use JavaScript with the DOM API for Dynamic Content or Behavior:

JavaScript is best for content that depends on user interaction, external data, or events. You'd typically use JavaScript to dynamically change the page or respond to user input.

Examples of when to use JavaScript and DOM manipulation:

Dynamically adding elements based on user interaction or server responses.
Creating interactive features like form validation, animations, or modals.
Fetching and rendering data from external APIs.
Updating part of the webpage without requiring a full reload.
Why? JavaScript allows for interactivity, responsiveness, and handling real-time data.

Example:

<!DOCTYPE html>
<html>
<head>
  <title>Dynamic Content</title>
</head>
<body>
  <button onclick="loadContent()">Click Me</button>
  <div id="content"></div>

  <script>
    function loadContent() {
      const div = document.getElementById("content");
      div.innerHTML = "<p>The content was dynamically added using JavaScript and the DOM API!</p>";
    }
  </script>
</body>
</html>
Best Practices: Finding the Balance
The best approach uses a combination of HTML/CSS and JavaScript:

HTML/CSS for the static, semantic structure and design of your site.
JavaScript and DOM manipulation only for dynamic interactions and content changes (e.g., animations, real-time updates, user interactions).
Why Not Use Only JavaScript and the DOM?
Performance: JavaScript-rendered content can be slower because the browser must dynamically generate and insert everything at runtime.
SEO: Search engines often struggle to index content that is dynamically loaded by JavaScript. Static HTML ensures search engines can index content easily.
Accessibility: Proper semantic HTML ensures accessibility. Creating content solely via JavaScript may break accessibility features like screen reader navigation.
Maintainability: Keeping markup and styles separate from behavior simplifies debugging and collaboration.
Summary
HTML/CSS: Define static structure and visual design that does not change dynamically.
JavaScript with DOM API: Handle dynamic interactions, real-time updates, and content changes.
Key Rule of Thumb: Use HTML/CSS for static and foundational design and JavaScript/DOM manipulation for dynamic, user-driven behaviors or real-time data fetching. This approach leads to faster performance, better SEO, improved accessibility, and easier maintenance.
