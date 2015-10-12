## Website Performance Optimization portfolio project

The objective is to optimize a specified online portfolio for speed. In particular, optimize the critical rendering path and make this page render as quickly as possible by applying the techniques picked up in the [Critical Rendering Path course](https://www.udacity.com/course/ud884).

### Getting started

URLs of the original version of the portfolio
* Repository: https://github.com/udacity/frontend-nanodegree-mobile-portfolio
* Live site: http://cameronwp.github.com/udportfolio

URLs of the optimized version of the portfolio
* Repository: https://github.com/icsantos/frontend-nanodegree-mobile-portfolio
* Live site: http://icsantos.github.io/frontend-nanodegree-mobile-portfolio/

#### Part 1: Optimize PageSpeed Insights score for index.html

##### Specification
Identify and perform optimizations to achieve a PageSpeed Insights score of 90 for both mobile and desktop.

##### Steps taken
* Resized and compressed pizzeria.jpg using Imagemagick
* Compressed profilepic.jpg using Imagemagick
* Changed Google Analytics script to async version
* Changed Google Webfonts from external link to inline CSS
* Changed style.css from external link to inline CSS

##### References
* [Efficient Image Resizing With ImageMagick](http://www.smashingmagazine.com/2015/06/efficient-image-resizing-with-imagemagick/)
* [Adding analytics.js to Your Site](https://developers.google.com/analytics/devguides/collection/analyticsjs/?hl=en)
* [Inline Google Fonts API CSS](https://developers.google.com/speed/pagespeed/module/filter-css-inline-google-fonts)

##### PageSpeed Insights Score
* 95/100 Mobile
* 97/100 Desktop

##### To check the PageSpeed Insights score and recommendations
* Open a browser tab or window
* Go to [PageSpeed Insights](https://developers.google.com/speed/pagespeed/insights/)
* Paste in this URL: http://icsantos.github.io/frontend-nanodegree-mobile-portfolio/
* Click on ANALYZE
* For comparison with the original version, repeat the above steps but paste in this URL: http://cameronwp.github.com/udportfolio

#### Part 2: Optimize Frames per Second in pizza.html

##### Specifications
* Identify and perform optimizations ensuring a consistent frame rate at 60fps when scrolling
* Time to resize pizzas in pizza.html is less than 5 ms as shown in the browser console
* Provide comments in views/js/main.js for pizza.html that effectively explain longer code procedures
* Provide a README file that documents the steps to run the application and explains the optimizations taken

##### Steps taken
* Used ImageMagick to resize pizza.png then tinypng.com to compress it
* Move capitalization to CSS
* Change querySelector() to getElementById()
* Change querySelectorAll() to getElementsByClassName()
* Move getElement* selectors outside of loops
* Move computation of new pizza size outside loop, basing the size on the first pizza only
* Reduce number of sliding pizzas to 20
* Used style.transform and translateX in place of style.left and basicLeft
* Minified main.js

##### References
* [Why Moving Elements With Translate() Is Better Than Pos:abs Top/left](http://www.paulirish.com/2012/why-moving-elements-with-translate-is-better-than-posabs-topleft/)

##### To check the frame rate and resize time of the optimized version
* Open up Google Chrome browser
* Go to the [live site]( http://icsantos.github.io/frontend-nanodegree-mobile-portfolio/) and click on "Cam's Pizzeria" or go directly to [Cam's Pizzeria](http://icsantos.github.io/frontend-nanodegree-mobile-portfolio/views/pizza.html)
* To open the DevTools
  - Select the Chrome menu at the top-right of your browser window, then select Tools > Developer Tools.
  - Right-click on any page element and select Inspect Element
  - Use CTRL + SHIFT + I (or CMD + OPT + I on Mac)
  - Press F12
  - More [shortcuts](https://developers.google.com/web/tools/iterate/inspect-styles/shortcuts)
* To check the resize time
  - If the console drawer is not visible, click on **>_** at the top-right of the DevTools window
  - In Cam's Pizzeria page, scroll down until you see the slider below the heading **Our Pizzas!**
  - Click the left or size side of the slider
  - The message `Time to resize pizzas:` followed by the time in milliseconds will display on the console
* To check the frame rate
  - Click on Timeline in the DevTools menu
  - To start recording a new timeline, click the record toolbar button at the top-left (below the search button) of the DevTools window, or press CTRL + E
  - While recording, scroll the Cam's Pizzeria page up and down a few times
  - Click the record toolbar button or press CTRL + E to stop recording
  - Select an area of interest in the overview by dragging.  Zoom and pan the timeline with the mousewheel or WASD keys
