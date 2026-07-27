**HTML Elements**

HTML elements are the basic building blocks of a webpage, defining its structure and content using start tags, content, and end tags.

# Note : html tags are not case-sensitive but for better practice lowercase tags are used...

**Nested HTML Elements**
Nested HTML elements occur when one element is placed inside another, creating a clear hierarchical structure for proper content organization and display.

* Nested elements create a parent–child hierarchy, which forms the structure of the DOM.
* Proper nesting improves accessibility, helping screen readers interpret content correctly.

# Block-Level Elements and Inline Elements

1. Block-Level Elements
Block-level elements start on a new line, occupy the full available width, stack vertically, and can contain both block-level and inline elements.

Examples

<div>: A general-purpose container for other elements.
<p>: Defines a paragraph.
<h1>, <h2>, ..., <h6>: Heading elements of different levels.
<ol>, <ul>: Ordered and unordered lists.
<table>: Defines a table.
<form>: Used for HTML forms to collect user inputs.
<section>, <article>, <nav>, <aside>, <header>, <footer>: Semantic elements that define areas of a webpage.

2. Inline Elements
Inline elements do not start on a new line, take only the width of their content, and are used within block-level elements to add or style content.

<span>: A general-purpose inline container for phrasing content.
<a>: Creates hyperlinks.
<img>: Embeds an image.
<strong>, <b>: Used for strong emphasis and bold text, respectively.
<em>, <i>: Used for emphasis and italic text, respectively.
<br>: Inserts a line break within text.
<input>: Creates interactive controls for forms.


**HTML Attributes**

HTML Attributes are special words used within the opening tag of an HTML element. They provide additional information about HTML elements. HTML attributes are used to configure and adjust the element's behaviour, appearance, or functionality in a variety of ways.

* Each attribute has a name and a value, formatted as name="value".
* Attributes tell the browser how to render the element or how it should behave during user interactions.

**Common HTML Attributes**

1. HTML alt Attribute
The alt attribute in HTML provides alternative text for an image if the image cannot be displayed. It improves accessibility and provides context for screen readers.

2. HTML width and height Attribute
The width and height Attribute is used to adjust the width and height of an image(in pixels).

3. HTML id Attribute
The id attribute in HTML assigns a unique identifier to an element, allowing it to be targeted by CSS and JavaScript for styling and manipulation purposes.

4. HTML title Attribute
The title attribute is used to explain an element by hovering the mouse over it. The behavior differs with various elements but generally, the value is displayed while loading or hovering the mouse pointer over it.

5. HTML href Attribute
The href attribute in HTML, used with the <a> tag, specifies a link destination. Clicking the linked text navigates to this address. Adding `target="_blank"` opens it in a new tab.

6. HTML style Attribute
The style attribute is used to provide various CSS effects to the HTML elements such as increasing font-size, changing font-family, coloring, etc.

7. HTML lang attribute
The language is declared with the lang attribute. Declaring a language can be important for accessibility applications and search engines.

**HTML Headings**

HTML headings are used to define the titles and subtitles of sections on a webpage. They help organize the content and create a structure that is easy to navigate.

* Proper use of headings enhances readability by organizing content into clear sections.
* Search engines use headings to understand page structure, which helps with SEO.

**HTML Paragraphs**

A paragraph in HTML is simply a block of text enclosed within the <p> tag. The <p> tag helps divide content into manageable, readable sections. It’s the go-to element for wrapping text in a web page that is meant to be displayed as a distinct paragraph.

* Adds space before and after the paragraph to visually separate it from other content.
* Breaks the text into a single block, creating an easy-to-read section.

**HTML Text Formatting**
HTML text formatting refers to the use of specific HTML tags to modify the appearance and structure of text on a webpage. It allows you to style text in different ways, such as making it bold, italic, underlined, highlighted, or struck-through.

1. Logical Tags
Logical tags convey the meaning or importance of the text without necessarily altering its visual appearance. These tags help browsers, search engines, and assistive technologies understand the purpose of the text.

<em>: Emphasizes text, typically rendered in italics. It implies that the text carries special importance or requires emphasis.
<strong>: Marks text as important, often displayed in bold. It implies the content is of strong importance.

2. Physical Tags
Physical tags directly affect how text looks on the webpage by changing the font, size, or style.

<b>: Displays text in bold without implying importance.
<i>: Italicizes text without any implied emphasis.

<i>	Showcases italicized text.
<small>	Renders text in a smaller font size.
<ins>	Highlights added or inserted text.
<sub>	Creates subscript text.
<strong>	Emphasizes text with importance, often in bold.
<b>	Displays text in a bold format.
<mark>	Accentuates text with a background highlight.
<del>	Strikes through text to signify deletion.
<em>	Adds emphasis to text, commonly styled as italic.
<sup>	Formats text as superscript.

**HTML Block Elements**
A block-level element always starts on a new line and stretches out to the left and right as far as it can i.e, it occupies the whole horizontal space of its parent element & the height is equal to the content's height.

<address>
<blockquote>
<dd>
<Div>
<dl> 
<dt>
<canvas>
<form>
<Heading>
<hr>
<li>
<main>
<nav>
<noscript>
<ol>
<pre>
<section>
<tfoot>
<ul>
<table>
<p>
<Video>
<aside>
<article>
<figcaption>
<fieldset>
<figure>
<footer>
<header>

**Inline Elements**
An inline element is the opposite of the block-level element. It does not start on a new line and takes up only the necessary width ie., it only occupies the space bounded by the tags defining the HTML element, instead of breaking the flow of the content. 

<br>
<button>
<time>
<tt>
<var>
<a>
<abbr>
<acronym>
<b>
<cite>
<code>
<dfn>
<em>
<i>
<output>
<q>
<samp>
<script>
<select>
<small>
<span>
<strong>
<sub>
<sup>
<textarea>
<bdo>
<big>
<img>
<input>
<kbd>
<label>
<map>
<Object>


**HTML Charsets**

HTML charsets define how characters are encoded so that text and symbols display correctly across different devices and browsers.

* Character encoding determines how text is represented and interpreted in an HTML document.
* The <meta> tag with the charset attribute specifies the encoding used by the webpage.
* Setting a charset ensures proper rendering of special characters and symbols.
* UTF-8 is the most commonly used charset as it supports multiple languages and symbols.

Common Character Encodings
Common character encodings define how text and symbols are represented for consistent display across devices and browsers.

1. ASCII
The American Standard Code for Information Interchange (ANSII) created this character encoding. This character encoding is used in C/C++ programming.

It has 128 alphanumeric characters consisting of alphabets(A-Z) and (a-z) and some special symbols like + - * / ( ) @ etc.

2. ANSI (Windows-1252)
American National Standards Institute (ANSI) created character encoding supported 256 characters. It is used as the default character set in Microsoft Windows. 

3. ISO-8859-1
It is used as the default character set of HTML4 and also supports 256 characters. The International Standards Organization (ISO) defines the standard character sets for different alphabets/languages. It contains numbers, upper and lowercase English letters, and some special characters. 

4. UTF-8
UTF-8 and UTF-16 standards was developed by Unicode Consortium, because the ISO-8859 character-sets are limited, and not compatible a multilingual environment. It consists all the character and punctuation symbols. 