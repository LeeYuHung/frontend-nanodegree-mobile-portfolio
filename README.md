# Website Performance Optimization portfolio project

This is the optimize version of the online portfolio. Read this file for more details.

## Grunt Project
***

#### What this project does
This grunt project creates minified css, javascript, html and image files.
Put the files to minified in the file type directories under the src directories(eg. All css files should be in ```src/css``` folder).You can find minified files in ```dist``` folder after you run the grunt.

#### Install and Run Project
1. Install the Grunt CLI. (Get more details from [here] (http://gruntjs.com/getting-started))
2. Change to the grunt directory.
3. Install project dependencies with ```npm install```.
4. Run Grunt with ```grunt```. 

## Optimization
***

#### index.html optimization

1. Inline the CSS into HTML using style tag.
2. Copress the images to the proper size.

#### pizza.html optimization

1. The for-loop in updatePositions function tried to get ```document.body.scrollTop``` repeatedly cause janky. So I declare a variable outside the loop and assign ```document.body.scroll``` to the variable. And inside the loop we can use the variable instead of calling ```document.body.scroll```.

2. In the changePizzaSizes function I moved the variable declaration ```dx``` and ```newwidth``` outside the loop. 