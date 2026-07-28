**CSS Introduction**

CSS (Cascading Style Sheets) is a language designed to simplify the process of making web pages presentable.

* It allows you to apply styles to HTML documents by prescribing colors, fonts, spacing, and positioning.
* CSS separates content from styling and enables reuse across pages.
* HTML uses tags, and CSS uses rule sets.
* CSS styles are applied to the HTML element using selectors.

# Cascading in CSS defines how the browser resolves conflicts between multiple CSS rules using importance, specificity, and source order.

1. CSS follows a hierarchy-Inline, Internal, External styles.
2. Specificity decides which selector has more weight.
3. Later rules override earlier ones if they have equal priority

**CSS combinators** define the relationship between two selectors. CSS selectors are patterns used to select elements for styling.

- A CSS selector can be simple or complex, consisting of more than one selector connected using combinators.

**Types of CSS Combinators**
1. General Sibling selector(~)
The general sibling selector selects elements that follow a specified element and share the same parent. This can be useful for selecting groups of elements with the same parent.
    div ~ p {

    }

2. Adjacent Sibling selector(+)
The adjacent sibling selector selects an element that is immediately next to a specified element. This selector selects only the next sibling.
    div + p {

    }

3. Child Selector(>)
The child selector selects elements that are direct children of a specified element. This combinator is stricter than the descendant selector, as it selects only the direct children.
    div > p{

    }

4. Descendant selector(space)
The descendant selector selects all elements that are descendants of a specified element. These elements can be any level deep within the specified element.

    div p{

    }

**CSS Selectors**
CSS Selectors are patterns used in CSS to select and target HTML elements so that styles can be applied to them. They define which elements on a web page should receive specific styling rules.

* Used to select HTML elements based on tag name, class, id, or attributes.
* Help apply styles like color, font, spacing, and layout.
* Make web pages structured, consistent, and visually appealing.

1. **Basic Selectors**

1. Universal Selector (*): Selects all elements on the page and applies the same style universally.
Example: Setting the font color for every element.
2. Element Selector: Targets all elements of a specific type, such as paragraphs or headers.
Example: Setting a common font size for all paragraphs
3. Class Selector (.): Applies styles to elements with a specific class attribute.
Example: Making all buttons have a blue background.
4. ID Selector (#): Styles a single element identified by its unique id.
Example: changing the background color of a header.

2. **Combinator Selectors**

1. Descendant Selectors: Targets an element inside another, such as paragraphs inside div .
Example: Styling paragraphs inside a div.
2. Child Selector (>): They only affects the direct child elements of a parent.
Example: Styling direct children paragraphs of a div.
3. Adjacent Sibling Selector (+): Styles an element immediately following another .
Example: Making the first paragraph bold after an h1.
4. General Sibling Selector (~): Styles all siblings that follow a specific element.
Example: Italicizing all paragraphs following an h1.

3. **Attribute Selectors**

1. Presence Selector: It selects elements that contain a specific attribute.
Example: styling all inputs with a type attribute.
2. Attribute Value Selector: It targets elements with a particular attribute value.
Example: Styling text inputs.
3. Substring Matching(^=): It matches elements where the attribute contains a substring.
Example: Styling links with https in their href.
4. Wildcard Selector (*=): Matches elements where the attribute value contains a specific string.
Example: Underlining links with example in the URL.
5. Ends With Selector ($=): Matches elements whose attribute value ends with a specific string.
Example: Styling links that end with .pdf in their URL.
6. Word Match Selector (~=): Matches elements whose attribute contains a specific whole word (space-separated).
Example: Styling elements that have the class highlight among multiple class names.
7. Hyphen Match Selector (|=): Matches elements whose attribute value starts with a word followed by a hyphen.
Example: Styling elements with language attributes like en or en-US.

4. **Pseudo-Classes**

1. :hover: Styles elements when the user hovers over them.
Example: Changing the color of a link when hovered.
2. :focus: Styles the elements when the user focus on any particular element.
3. :first-child: Styles the element which is the first child of it's parent.
4. :last-child: Style's the element which is the last child of it's parent.
5. :not: Helps to remove a particular element from the styling index or styling context.

5. **Pseudo-Elements**

1. ::before: To insert some content before an element.
2. ::after: To insert some content after an element.
3. ::first-line: Styles the first line of text within a block element. Line breaks mark the beginning of a new line.
4. ::first-letter: It Styles the first-letter of a word or a sentence.
5. ::placeholder: Styles the placeholder of a specific input field.
