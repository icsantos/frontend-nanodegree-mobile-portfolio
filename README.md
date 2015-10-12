## Website Performance Optimization portfolio project

The objective is to optimize a specified online portfolio for speed. In particular, optimize the critical rendering path and make this page render as quickly as possible by applying the techniques picked up in the [Critical Rendering Path course](https://www.udacity.com/course/ud884).

### Getting started

Download the [required project assets](https://github.com/udacity/frontend-nanodegree-mobile-portfolio).

####Part 1: Optimize PageSpeed Insights score for index.html

Specification
-------------
Identify and perform optimizations to achieve a PageSpeed Insights score of 90 for both mobile and desktop.

Steps taken
-----------
* Resized and compressed pizzeria.jpg using Imagemagick
* Compressed profilepic.jpg using Imagemagick
* Changed Google Analytics script to async version
* Changed Google Webfonts from external link to inline CSS
* Changed style.css from external link to inline CSS

References
----------
* http://www.smashingmagazine.com/2015/06/efficient-image-resizing-with-imagemagick/
* https://developers.google.com/analytics/devguides/collection/analyticsjs/?hl=en
* https://developers.google.com/speed/pagespeed/module/filter-css-inline-google-fonts

PageSpeed Insights Score
------------------------
* 95/100 Mobile
* 97/100 Desktop

####Part 2: Optimize Frames per Second in pizza.html

Specifications
--------------
* Identify and perform optimizations ensuring a consistent frame rate at 60fps when scrolling
* Time to resize pizzas in pizza.html is less than 5 ms as shown in the browser console
* Provide comments in views/js/main.js for pizza.html that effectively explain longer code procedures
* Provide a README file that documents the steps to run the application and explains the optimizations taken

Steps taken
-----------
* Used ImageMagick to resize pizza.png then tinypng.com to compress it
* Move capitalization to CSS
* Change querySelector() to getElementById()
* Change querySelectorAll() to getElementsByClassName()
* Move getElement* selectors outside of loops
* Move computation of new pizza size outside loop, basing the size on the first pizza only
* Reduce number of sliding pizzas to 20
* Used style.transform and translateX in place of style.left and basicLeft
* Minified main.js

References
----------
http://www.paulirish.com/2012/why-moving-elements-with-translate-is-better-than-posabs-topleft/

