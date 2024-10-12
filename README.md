# Silent URL Cleaner and Copier Bookmarklet

## Description
This repository contains a compact, efficient JavaScript bookmarklet that silently removes query parameters from the current URL and copies the cleaned URL to the clipboard. It's designed for users who frequently need to share clean URLs without the clutter of tracking parameters or session information.

## Features
- Removes all query parameters from the current URL
- Copies the cleaned URL to the clipboard
- Updates the browser's address bar without page reload
- Operates silently without any dialog boxes or visible notifications
- Lightweight and fast, requiring no external dependencies

## Usage
1. Create a new bookmark in your browser
2. Name it "Silent Clean & Copy URL" (or any preferred name)
3. In the URL field of the bookmark, paste the following code:

```javascript
javascript:(function(){var u=new URL(location.href);u.search='';history.replaceState({},'',u);navigator.clipboard.writeText(u.toString());})();
```

4. Click the bookmark on any web page to clean the URL and copy it to your clipboard

## Technical Details
- Utilizes the `URL` API for robust URL parsing and manipulation
- Employs `history.replaceState()` to update the URL without triggering a page reload
- Uses the modern `navigator.clipboard` API for clipboard operations
- Compatible with most modern web browsers that support these JavaScript APIs

## Use Cases
- Sharing URLs in professional settings without exposing session or tracking information
- Cleaning URLs for documentation or reporting purposes
- Quickly generating clean links for social media sharing
- Streamlining URL management in web development and testing processes

## Notes
- This bookmarklet operates silently and provides no visual feedback. Users should verify the clipboard contents if confirmation is needed.
- Clipboard operations may require appropriate permissions in some browsers.

## Contributions
Contributions, issues, and feature requests are welcome. Feel free to check [issues page] if you want to contribute.

## License
[MIT License](LICENSE)

---

Created by Pete Cohen - building on the work of someone else (I can't remember who, sorry!) and iterating with the help of Claude Sonnet 3.5
