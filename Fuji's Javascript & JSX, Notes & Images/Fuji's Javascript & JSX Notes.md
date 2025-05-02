---
share: true
---
These are my personal notes for learning Javascript/Javascript-related stuffs

# JSX (Javascript Markup/Syntax)
JSX is a Syntax Extension for Javascript that lets you write HTML-like markup inside a JavaScript file. Although there are other ways to write components, most React developers prefer the conciseness of JSX, and most codebases use it.

The Web has been built on HTML, CSS, and JavaScript. For many years, web developers kept content in HTML, design in CSS, and logic in JavaScript—often in separate files! Content was marked up inside HTML while the page’s logic lived separately in JavaScript:
![Pasted image 20250501060316.png](Pasted%20image%2020250501060316.png#)
But as the Web became more interactive, logic increasingly determined content. JavaScript was in charge of the HTML! This is why **in React, rendering logic and markup live together in the same place—components.**
![Pasted image 20250501060349.png](Pasted%20image%2020250501060349.png#)
Keeping a button’s rendering logic and markup together ensures that they stay in sync with each other on every edit. Conversely, details that are unrelated, such as the button’s markup and a sidebar’s markup, are isolated from each other, making it safer to change either of them on their own.

Each React component is a JavaScript function that may contain some markup that React renders into the browser. React components use a syntax extension called JSX to represent that markup. JSX looks a lot like HTML, but it is a bit stricter and can display dynamic information. The best way to understand this is to convert some HTML markup to JSX markup.


## Exports: Default Vs. Named
In JavaScript, there are 2 primary (not only) ways to export values: Default Exports, and Named Exports. You can use one or both in the same file. **A file can have no more than 1 Default Export, but it can have as many Named Exports as you like.**
![Pasted image 20250430080848.png](Pasted%20image%2020250430080848.png#)
Depending on how you export your Component dictates how you MUST import it, or else you will get an error using the wrong imports and exports. (Button can be replaced with any Text.)
![Pasted image 20250430081043.png](Pasted%20image%2020250430081043.png#)
![Pasted image 20250501054333.png](Pasted%20image%2020250501054333.png#)
![Pasted image 20250501054347.png](Pasted%20image%2020250501054347.png#)
As seen in **App.js**, while the **Import** for **Gallery** remained the same name because it was a **Default Function export**, the **Named Function** of **Profile** had to be **specified with the Curly Brackets** in order for one of its **functions** to appear and render-able by the later **Default Function App**.  

## Parent and Child codes
Because it becomes easier when codes are done from an original source to later sources, you need to organise them as Parent and Child. For an Array to use an image as part of its coding, an Array must find the image itself being available to upload.
![Pasted image 20250427002318.png](Pasted%20image%2020250427002318.png#)![Pasted image 20250427002342.png](Pasted%20image%2020250427002342.png#)
With code being case-sensitive, sections with Capital Letters should be left as Names for named sections on pages, call backs to previously named functions, or for text within headers or specified areas.

Function - This section of code defines  something with a Name.
Export default - This is a 'prefix' of standard JavaScript syntax; you mark a main function so you can later import it from other files.

The code above leads to this result:
![Pasted image 20250430064149.png](Pasted%20image%2020250430064149.png#)
Each whole section of code is called a Component, each with their own purposes. They're usually found in a Root Component File usually named App.js; depending on setups, it could be in another file, or have a different name.
## Brackets - Starts and Ends
Using one of the following brackets, you can use your script to define, search, and continue chains of code for an array:
- ( ) - Circle Brackets
- <> - Triangle Brackets
- { } -  Curly Brackets
- \[] - Square Brackets
## Exporting and Importing Components
To make certain functions more modular and reusable in other files, the following should be done:
- Make a JS file (JavaScript) to put the components in
- Export the function components from the Root File (using either default of named exports)
- Import the component into the new JS file where I'll be using the component using the below method.
E.g. Both the Profile and Gallery Components have been moved out from App.js into the new JS file called Gallery.js. Now you can have App.js import Components from Gallery.js (The original code in App.js was moved to Gallery.js, and)
![Pasted image 20250430071016.png](Pasted%20image%2020250430071016.png#)
![Pasted image 20250430071048.png](Pasted%20image%2020250430071048.png#)
Breakdown of what's accomplished:
- Gallery.js
	- Defines 'Profile' component which can only be used within the same file without exporting it 
	- Exports the 'Gallery' component as a Default Export
- App.js
	- Imports 'Gallery' as a Default Import from 'Gallery.js' (Either './Gallery' or 'Gallery.js' works on on more current day models, but older code may require specification)
	- Exports the Root 'App' component as a Default Export
Default Imports can have any name for your 'Import' after you make your 'Import' like 'import Banana from './Button.js' instead and still get the same Default Export. Named Imports, however, have to match on both sides.

Regardless of the coding style, always give meaningful names to your Component Functions and Files that contain them. Trying to debug stuff like 'export default () => {}' just makes debugging unnecessarily harder.