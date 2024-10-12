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
