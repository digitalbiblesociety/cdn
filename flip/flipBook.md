To disable both the FlipSound and SlideSound across all your books by editing the config.js file, you can use a find and replace command in a code editor or text-processing tool.

Steps:
Find the configuration options related to sound.

enableFlipSound
FlipSound
enableSlideSound (if applicable)
Replace their values.

Set these options to false.
Here’s the find and replace command you can use:

Find:
javascript
Copy code
"enableFlipSound":\s*["']?true["']?,
"FlipSound":\s*["']?true["']?
Replace:
javascript
Copy code
"enableFlipSound": false,
"FlipSound": false
Explanation:
The \s* allows for any whitespace between the key and value.
The ["']? matches optional quotes around the value.
Usage:
If you're using VS Code:

Open the config.js file.
Press Ctrl + F to open the search bar.
Click on the ... icon or press Ctrl + H to enable "Replace" mode.
Paste the Find pattern in the search bar and the Replace pattern in the replace bar.
Enable "Match Case" and "Use Regular Expressions" (usually denoted by a .* icon).
Click "Replace All."
For a command-line tool like sed:

bash
Copy code
sed -i 's/"enableFlipSound":\s*["']?true["']?,/"enableFlipSound": false,/g' config.js
sed -i 's/"FlipSound":\s*["']?true["']?/"FlipSound": false/g' config.js
Save the changes and re-upload the modified config.js file to apply the updates to your FlipHTML5 books.