## Website Performance Optimization portfolio project

- Julie Rezazadeh

The challenge of this project was to optimize the online portfolio given to us for speed! 
In particular, we were to optimize the critical rendering path and make the page given render as quickly as possible by applying the techniques that we've learned. 


### Part 1: Optimize PageSpeed Insights score for index.html

The first specification in the rubric states that you need your index.html page to achieve a PageSpeed score of at least 90 for Mobile and Desktop.


To allow for an easy pageSpeed test, I've used github's webpages to host my project directly from my github repository.


Steps to check the pageSpeed score on mobile and desktop

1. In your search bar, navigate to https://developers.google.com/speed/pagespeed/insights/

2. Upon entering this site, you will see a textbox field that asks you to Enter a webpage URL

3. The exact site name that you will be confirming has the correct pageSpeed of 90 is
http://julierezazadeh.github.io/dist/

4. Once you've hit Analyze, the page will then provide you will the Mobile and Desktop pageSpeed (which are kept in two separate tabs)  

This score represents how quickly your page has been ran. 




To allow for successful completion of this section I've changed a few things in the index.html file that was provide.
-  All images on this page have been compressed to a smaller file size. (http://compresspng.com/ , http://compressjpeg.com/)
-  Asynchronous loading all of the <script> tags of JavaScript using the 'async' tag 
-  Inlined all the CSS that was in the print.css and style.css folder for faster pageSpeed
-  Minified all the files for distribution mode



### Part 2: Optimize Frames per Second in pizza.html

To optimize views/pizza.html, I have modified views/js/main.js until the frames per second rate reached 60 fps or higher when scrolling. You will find instructive comments in main.js. 


Steps to check to FPS
- Navigate to julierezazadeh.github.io to check the FPS 
- Click the link that reads 'Cam's Pizzeria', this will navigate to the page that needs a specific FPS score.
- ctrl-shift-i to open dev tools, or right click on the page and click inspect.
- Select the Console tab to view the Average scripting time to generate last 10 frames and time to generate pizzas on load. 
- In the performance tab, start recording the page. If you're unfamiliar with how to record check out this website! https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/reference
- Once you've finished recording the scrolling of the page, you will find some useful information that dev tools provides
- Look for the green bars to check the FPS!

To allow for successful completion of the section I've outlined a few of the changes I've made in this file to help reach the 60FPS mark. 
(Found in the views/js/main.js file)
- Changing all querySelectors to getElementById and querySelectorAll to getElementsByClassName because I came across multiple articles stating that in most cases this will allow the program to run faster (https://jsperf.com/getelementbyid-vs-queryselector)
- Removed deprecated properties
- Removed some properties out of the for loops they were in because there wasn't a point in having the same number loop x amount times. 
- It appeared that the highest number of pizzas in the background that can be shown on the screen was 32, (8 across x 4 down) so I changed the for loop to only loop through the ones showing on the screen (32) instead of 200 which did extra work for no reason.
- I also deleted or added some of the elem styles in the last for loop in the document to a .mover css class in pizza.html







