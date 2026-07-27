**HTML Colors**

**Color Values**
Color values in HTML define the color of elements. They can be specified using various formats such as hexadecimal, RGB, RGBA, HSL, HSLA, color names, and system color keywords.

1. RGB Color Value
RGB, which stands for Red, Green, and Blue, is a method used in CSS to describe colors. It works by mixing different amounts of three primary colors, each with values ranging from 0 to 255. By adjusting these values, we can produce an extensive range of colors, allowing for the creation of diverse and better color palettes across websites. 

2. RGBA Color Value
RGBA (Red, Green, Blue, Alpha) is a color model similar to RGB, but with an added alpha parameter representing transparency. The alpha value, which ranges from 0 to 1, adjusts transparency, allowing the display of colors with varying levels of opacity. It's representation is as rgba(red, green, blue, alpha).

3. HEX Color Value
Hexadecimal color values, often referred to as hex values, use a six-digit code made up of pairs of characters.

* Hexadecimal values in CSS are represented as #rrggbb, where rr, gg, and bb denote the intensity of red, green, and blue, respectively, ranging from 00 to ff.
* This encoding allows for 16,777,216 unique color combinations, providing a vast spectrum for web design.
* For example, #ff0000 corresponds to red (max red, no green, no blue), while #00ff00 represents green (max green, no red, no blue).
* Black is denoted by #000000 (no red, no green, no blue), while white is represented as #ffffff (max red, max green, max blue).

4. HSL (Hue, Saturation, Lightness) Value
HSL color values in HTML represent colors by defining their hue, saturation, and lightness. The hue signifies the type of color (red, blue, green, etc.), saturation refers to the intensity or purity of the color, and lightness determines the brightness or darkness.

HSL Color value Properties:
* HSL representation defines colors based on Hue, Saturation, and Lightness components, offering a more intuitive way to specify colors.
* Hue represents the color type, ranging from 0 to 360 degrees.
* Saturation determines the intensity or purity of the color, from 0% (grayscale) to 100% (full color).
* Lightness controls the brightness of the color, ranging from 0% (black) to 100% (white), with 50% representing normal.

**HTML Links Hyperlinks**
HTML Links, also known as Hyperlinks, are used to connect one web page to another, allowing users to navigate easily between different pages, websites, or sections within the same page.

* The <a> (anchor) tag creates hyperlinks, using the href attribute to specify the destination URL.
* It can link text, images, or buttons for navigation.
* Links can open in the same tab or a new tab using the target attribute, and other common attributes include title for additional information.

1. _blank	Opens the linked document in a new window or tab.
2. _self	Opens the linked document in the same frame or window as the link. (Default behavior)
3. _parent	Opens the linked document in the parent frame.
4. _top	Opens the linked document in the full body of the window.
5. framename	Opens the linked document in a specified frame. The frame’s name is specified in the attribute.

**HTML Images**
The HTML <img> tag is used to embed an image in web pages by linking them. It creates a placeholder for the image, defined by attributes like src, width, height, and alt, and does not require a closing tag.

There are two ways to insert the images into a webpage:
* By providing a full path or address (URL) to access an internet file.
* By providing the file path relative to the location of the current web page file.

**HTML Favicon**
A favicon is a small image displayed next to a website’s title in the browser tab. It helps users quickly recognize and return to a website.

* Appears in browser tabs, bookmarks, and browsing history for easy identification.
* Improves brand recognition by serving as a visual identity for the website.
* Enhances the professionalism and credibility of the site.
* Improves usability by helping users locate their tab among multiple open tabs.

# Creating and Adding a Favicon
To create and add a favicon to your website, follow these simple steps to ensure it's displayed properly across different browsers and devices:

1. Design a small favicon image (usually 16×16 or 32×32 pixels) and save it in formats like .ico, .png, or .svg.
2. Upload the favicon image to your website’s root directory or use an external image URL.
3. Add a <link> tag inside the <head> section of your HTML file to reference the favicon.
4. Save the changes and test the favicon by opening the website in a browser to ensure it displays correctly.

**HTML Video**
The <video> element in HTML is used to show video content on web pages. It supports various video formats, including MP4, WebM, and Ogg. It is introduced in HTML5.

Syntax : 
<video src="" controls>   </video>
               or
<video controls="controls">
<source src="video_filename" type="video_type">
 </video>

 