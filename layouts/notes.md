The color of a specific page could be changed **without** directly editing the theme by:

> Add a few lines of custom JS to check for the required page name in the URL and
> then set style property of body to the desired background color 

What this means:
* Locate the file in the `layouts` section that controls the LOOK of the page in
  question.
* Write some custom javascript to analyze the URL of the page. Here's what the
  pseudocode would look like. NOTE THIS IS NOT REAL JAVASCRIPT
  ```
  if currentPage.URL == "./para-series":
    return body {
        background-color: black;
        text-color: white;
    }
  ```
* Change the css for that specific element.

> overriding layouts/_default/baseof.html (i.e. copy
> themes/academic/layouts/_default/baseof.html to layouts/_default/baseof.html
> creating the folders as necessary) and adding some Go templating logic to set
> the style property of body to the desired background color

What this means: