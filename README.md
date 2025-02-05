# Race Condition in HTML DOM Access

This repository demonstrates a subtle race condition that can occur when JavaScript code attempts to access a DOM element before the browser has fully parsed and rendered the HTML.  This is an uncommon but important error that highlights the timing issues in web development.

## Description

The `bug.html` file contains a simple HTML page with a `<div>` element.  A JavaScript script attempts to update the `innerHTML` of this div before the browser is finished rendering the page. This results in a runtime error because the script is trying to access an element that doesn't yet exist in the DOM.

The `solution.html` shows how to solve this issue using the `DOMContentLoaded` event, ensuring that the script runs only after the HTML document is fully loaded.