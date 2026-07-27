**HTML Tables**

HTML tables help organize data into rows and columns, making information easy to read and compare. They are useful for displaying schedules, price lists, product details, and more.

* Can include text, images, links, and other elements.
* Built using tags like <table>, <tr>, <th>, and <td>.
* Allow clear presentation of data for comparison.
* Can be styled with CSS for better design and readability.

1. Adding a Border to an HTML Table
Syntax:

table, th, td {
      border: 1px solid black;
}

2. Adding Collapsed Borders in an HTML Table
Syntax:

 table, th, td {
       border: 1px solid black;
       border-collapse: collapse;
 }

3. Adding Cell Padding in an HTML Table
Syntax:

th, td {
        padding: 20px;
}

4. Adding Left Align Headings in an HTML Table
Syntax:

th {
      text-align: left;
}

5. Adding Border Spacing in an HTML Table
Syntax:

table {
      border-spacing: 5px;
}

6. Adding Cells that Span Many Columns in HTML Tables
7. Adding Cells that span many rows in HTML Tables

8. Adding a Caption in an HTML Table
Syntax:

<table style="width:100%">
<caption>DETAILS</caption>

9. Adding a Background Color to the Table
Syntax:

table#t01 {
            width: 100%;
            background-color: #f2f2d1;
}

10. Creating Nested Tables


**HTML iframes**
An iframe, or Inline Frame, is an HTML element represented by the <iframe> tag. It functions as a 'window' on your webpage through which visitors can view and interact with another webpage from a different source.

iframes are used for various purposes like:
* Embedding Multimedia: Easily integrate videos, audio, or animations from platforms like YouTube, etc.
* Including Maps: Embed maps from services like Google Maps directly into your site.
* Loading Forms and Widgets: Incorporate forms or widgets from other sources without writing complex code.

Syntax:
<iframe src="URL" title="description"></iframe>


**HTML Layout**
HTML layouts divide a web page into structured sections for better organization and styling. They improve readability, accessibility, and overall user experience.

* Semantic Structure: Uses elements like <header>, <nav>, <main>, <article>, <section>, <aside>, and <footer>.
* Better Organization: Helps arrange content clearly, making pages easier to manage.
* Improved SEO & Accessibility: Enhances search engine understanding and user accessibility.

Syntax : 
<header> Content... </header>
<nav> Content... </nav>
<main> Content... </main>
<footer> Content... </footer>


**HTML File Paths**
HTML file paths specify the location of resources like images, videos, scripts, and documents so the browser can load them correctly.

* Help the browser locate and load external resources.
* Used for files such as images, videos, scripts, and documents.
* Specified using attributes like src and href.

Types of File Paths
1. Absolute File Paths
It specifies the full URL or complete location of a resource, starting from the root of the website or including the domain name.

Syntax:
<img src="https://media.geeksforgeeks.org/wp-content/uploads/geek.png" alt="My Image">

2. Relative File Paths
Relative file paths locate resources based on the HTML file’s location, keeping links portable.

Syntax:
<img src="images/geeks.jpg" alt="My Image">