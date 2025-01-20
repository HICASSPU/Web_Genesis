# Web Genesis: Day 1 - Web Development Foundations

Welcome to Day 1 of Web Genesis! 🎉 Today, we'll embark on a journey into the heart of web development, exploring the foundational trio: HTML, CSS, and JavaScript. By the end of this session, you'll have a solid grasp of how web pages are constructed and be equipped to create your very own!

## 1. Understanding the Web

* The web operates on a **client-server** model:
    * **Client:** Your web browser (e.g., Chrome, Firefox) acts as the client.
    * **Server:** A powerful computer that stores the web page's files.
    * **Communication:** Happens through protocols like **HTTP** (Hypertext Transfer Protocol) and **HTTPS** (for secure connections).

* **Key Terms:**
    * **URL (Uniform Resource Locator):** The web address of a specific resource (e.g., [https://www.google.co.uk/](https://www.google.co.uk/)).
    * **DNS (Domain Name System):** Translates human-readable URLs into machine-readable IP addresses.
    * **HTTP Methods:** 
        * **GET:** Retrieve data from the server.
        * **POST:** Send data to the server (e.g., form submissions).
        * **PUT:** Update data on the server.
        * **DELETE:** Remove data from the server.

## 2. HTML (HyperText Markup Language)

* HTML is the **foundation** of any webpage. It uses **elements** (tags) to structure content.

* **Key Concepts:**
    * **Basic Tags:**
        * **Headings:** `<h1>` to `<h6>` (for different levels of importance).
        * **Paragraphs:** `<p>`.
        * **Links:** `<a href="URL">` (e.g., `<a href="https://www.example.com">Visit Example</a>`).
        * **Images:** `<img src="image.jpg" alt="Description of the image">` (always use the `alt` attribute for accessibility).
        * **Lists:** 
            * Unordered lists: `<ul>` with `<li>` for each item.
            * Ordered lists: `<ol>` with `<li>` for each item.
    * **Attributes:** Provide extra information about elements (e.g., `src` for image source, `href` for link destination, `alt` for image description).
    * **Semantic HTML:** Using meaningful tags like `<header>`, `<nav>`, `<main>`, `<footer>` to improve readability and accessibility for both humans and machines.

* **Activity:**
    1. Create a new file named `index.html`.
    2. Add the basic HTML structure:
       ```html
       <!DOCTYPE html>
       <html>
       <head>
           <title>My First Web Page</title> 
       </head>
       <body>
           </body>
       </html>
       ```
    3. Inside the `<body>`:
        * Add a level 1 heading (e.g., `<h1>Welcome to My Page!</h1>`).
        * Add a paragraph about yourself.
        * Create an unordered list of your favorite hobbies.
        * Include an image (make sure to provide the correct image source).
        * Add a link to your favorite website.

## 3. CSS (Cascading Style Sheets)

* CSS controls the **appearance** of HTML elements (colors, fonts, layout, etc.).

* **Key Concepts:**
    * **Selectors:** 
        * **Tag selectors:** (e.g., `p { color: blue; }` - styles all paragraph elements)
        * **Class selectors:** (e.g., `.myClass { font-size: 20px; }` - styles elements with the "myClass" class)
        * **ID selectors:** (e.g., `#myId { background-color: yellow; }` - styles the element with the ID "myId")
    * **Box Model:** Understand how width, height, padding, border, and margin affect how elements are displayed.
    * **Responsive Design:** Using **media queries** to adapt the layout to different screen sizes (e.g., desktops, tablets, mobile phones).

* **Activity:**
    1. Create a new file named `style.css`.
    2. Write CSS rules to:
        * Change the background color of the page.
        * Center-align the text.
        * Add padding around the content.
        * Change the color and font size of headings.
    3. Link the CSS file to your `index.html` using:
       ```html
       <link rel="stylesheet" href="style.css">
       ```

## 4. JavaScript: Adding Interactivity

* JavaScript brings **behavior** to your web pages, making them dynamic and responsive.

* **Key Concepts:**
    * **Variables:** Store data (e.g., `let name = "John";`, `const pi = 3.14159;`).
    * **Functions:** Reusable blocks of code (e.g., `function greet() { alert("Hello!"); }`).
    * **DOM Manipulation:** Use JavaScript to access and manipulate HTML elements (e.g., change text, add/remove elements, handle events).

* **Activity:**
    1. Create a new file named `script.js`.
    2. Add a button to your `index.html`:
       ```html
       <button onclick="showAlert()">Click Me</button>
       ```
    3. In `script.js`, write a function that displays an alert when the button is clicked:
       ```javascript
       function showAlert() {
           alert("You clicked the button!");
       }
       ```
    4. Link the JavaScript file to your `index.html`:
       ```html
       <script src="script.js"></script>
       ```

## 5. Putting It All Together: Your Personal Intro Page

* **Project Structure:**
    * Create a new folder for your project (e.g., "my-intro-page").
    * Inside the folder, create:
        * `index.html`
        * `style.css`
        * `script.js`

* **Goal:** Create a simple webpage about yourself that showcases your newfound HTML, CSS, and JavaScript skills.

* **Requirements:**
    * **HTML:**
        * Add a heading with your name.
        * Include a paragraph introducing yourself.
        * Create an unordered list of your hobbies.
        * Add an image of yourself (or something you enjoy).
    * **CSS:**
        * Style the text (font, color, size).
        * Add a background color to the page.
        * Apply some basic styling to the elements

**References:**

* **MDN Web Docs:** https://developer.mozilla.org/ - Comprehensive documentation for HTML, CSS, and JavaScript.
* **W3Schools:** https://www.w3schools.com/ - Easy-to-follow tutorials and references for web development technologies. 

## *Created by:*

*Atharva Wakodikar*

---

## *Contributing*

Feel free to contribute by suggesting edits, adding more resources, or sharing your learning experiences.