# vscode-user-snippet
## A VS Code User Snippet Example

### Example Creating a Snippet for a Bootstrap Navbar
> In this example, we will create a Global User Snippet for a Bootstrap Navbar to be used ("scoped") in html and django-html files in vscode. Additionally, this guide uses a neat editing feature in vscode called Multiple selections (multi-cursors).
1. `File > Preferences > Configure User Snippets` (`Code > Preferences` on macOS)
2. Select `New Global Snippets File`
3. Name the file `bootstrap-navbar` (*it will save as `bootstrap-navbar.code-snippet`*)
> Snippets files are written in JSON, support C-style comments, and can define an unlimited number of snippets. Snippets support most TextMate syntax for dynamic behavior, intelligently format whitespace based on the insertion context, and allow easy multiline editing.
4. Create the snippet object
```
{
	"Bootstrap 5.0 Navbar": {
		"scope": "html, django-html",
		"prefix": "bootnav",
		"body": [
			"code goes here",
		],
		"description": "Example Bootstrap 5.0 Navbar from https://getbootstrap.com/docs/5.0/components/navbar/"
	}
}
```
5. Copy the bootstrap example code (*see the references for a link to the code)
6. Highlight the entire line `"code goes here",` to include the leading indentation on that line)
7. Paste in the Bootstrap example code
> *The HTML code has quotation marks that will need to be escaped for this JSON file type*
8. Highlight the Bootstrap example code
9. Find and Replace in the selection `"` with `\"`
> <!> Make sure word wrap is off before using multiline cursor in next step
10. Format the multiline bootstrap code as strings for JSON files using Multi-cursors
    - Place your cursor at the beginning of the first line of Bootstrap example code, right before the `<nav>`
    - Add multi-cursors to the beginning of each line of Bootstrap example code
        - PC [Ctrl] + [Alt] + [Down] until you reach the last line of Boostrap example code
        - macOS [Cmd] + [Option] + [Down] until you reach the last line of Boostrap example code
    - With your multi-cursors at the beginning of each line type `"`
    - Move your multi-cursors to the end of each line
        - PC [end]
        - macOS [Fn] + [Right]
    - With your multi-cursors at the beginning of each line type `",`
    - For proper JSON formatting, remove the comma of the last element of our Bootstrap code
11. [Example snippet final code](https://github.com/zaxx81/vscode-user-snippet/blob/main/boostrap-nav.code-snippets)

### References
1. [Snippets in Visual Studio Code](https://code.visualstudio.com/docs/editor/userdefinedsnippets)
2. [Basic Editing - Multiple selections (multi-cursor)](https://code.visualstudio.com/docs/editor/codebasics#_multiple-selections-multicursor)
3. [Bootstrap 5.0 Navbar Example](https://getbootstrap.com/docs/5.0/components/navbar/)
