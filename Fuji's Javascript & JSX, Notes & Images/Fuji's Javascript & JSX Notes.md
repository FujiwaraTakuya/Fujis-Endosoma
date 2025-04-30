---
share: true
---
These are my personal notes for learning Javascript/Javascript-related programs

# JSX (Javascript Markup/Syntax)
## Exports: Default Vs. Named
In JavaScript, there are 2 primary (not only) ways to export values: Default Exports, and Named Exports. You can use one or both in the same file. **A file can have no more than 1 Default Export, but it can have as many Named Exports as you like.**
![Pasted image 20250430080848.png](Pasted%20image%2020250430080848.png#)
Depending on how you export your Component dictates how you MUST import it, or else you will get an error using the wrong imports and exports. (Button can be replaced with any Text.)
![Pasted image 20250430081043.png](Pasted%20image%2020250430081043.png#)

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
- \[ ] - Square Brackets
## Exporting and Importing Components
To make certain functions more modular and reusable in other files, the following should be done:
- Make a JS file (JavaScript) to put the components in
- Export the function components from the Root File (using either default of named exports)
- Import the component into the new JS file where I'll be using the component using the below method.
E.g. Both the Profile and Gallery Components have been moved out from App.js into the new JS file called Gallery.js. Now you can have App.js import Components from Gallery.js (The original code in App.js was moved to Gallery.js, and)
![Pasted image 20250430071016.png](Pasted%20image%2020250430071016.png#)
![Pasted image 20250430071048.png](Pasted%20image%2020250430071048.png#)
Breakdown of what's accomplished
- Gallery.js
	- Defines 'Profile' component which can only be used within the same file without exporting it 
	- Exports the 'Gallery' component as a Default Export
- App.js
	- Imports 'Gallery' as a Default Import from 'Gallery.js' (Either './Gallery' or 'Gallery.js' works on on more current day models, but older code may require specification)
	- Exports the Root 'App' component as a Default Export