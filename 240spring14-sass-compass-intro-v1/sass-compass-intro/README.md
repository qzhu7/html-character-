The purpose of these files is to provide some general examples of one way to set up a sass project.

These files are set up specifically for our class project but there are also general ideas you can use in other projects.

## Sass Setup and Resources

You will have to setup Sass to do anything here. This documentation doesn't explain the setup. If you need help try these:

* Official Sass Installation Guide: [http://sass-lang.com/install](http://sass-lang.com/install)
* Official [Sass](http://mhs.github.io/scout-app/) Documentation: 
* Official Compass Documentation: [http://compass-style.org/reference/compass/](http://compass-style.org/reference/compass/)

## What&rsquo;s in this Repository

Here is a description of the files included.

### Folder Structure
There are two folders, __css__ and __scss__. The basic workflow is that you write Sass files in the scss folder and then Sass compiles them into CSS and puts them in the css folder. 

So, **Never Write anything in the css folder**

### Files in SCSS folder

`style.scss`  
This is the main stylesheet. In the current setup it imports all of the other files (partials). You will notice that there is no actual css in this file, just the imports

#### Partials
All of the remaining files are called partials. They are called this because they are designed to be a **part** of the full CSS file. Sass will only compile these files if they are imported into another file.

You set a file as a partial by putting an underscore _ in the front of it.

`_reset.scss`  
This is just a copy of [Eric Meyer's reset stylesheet](http://meyerweb.com/eric/tools/css/reset/reset.css). We use it in this class, instead of something like [Normalize](http://necolas.github.io/normalize.css/), so you have to make all of the decisions about font-size, padding, margin etc.

`_variables.scss`  
Sass allows you to write variables and set things like colors and widths. You aren't limited to writing variables here, but some people like putting most of them in one place so they are easier to find. The only variables I didn't include here are ones used specifically for mixins.

`_mixins.scss`  
Mixins are a kind of function for CSS (Sass also has actual functions). Mixins allow us to more easily write things like media queries and CSS grids.

`_global.scss`  
This is where we will store styles that are used on every page of the site. body, p, h1..h6, ul, li and so on can be set here. It is where you do things like setup the default typography for the site.

`_navigation.scss`  
Because navigation can be complex and may even require its own breakpoints we separated it out into its own file instead of putting it in _global.scss

#### Page Specific CSS  
The following files are where you can place page specific CSS. I included the six pages for this site. If you added more pages or had a different site you would modify these.

Each page has styles that relate just to that page. In the workflow I will show in class, this is where a lot of the media query and grid work will go because that is specific to each page.

I only imported index and schedule and left the other four for you to do to practice writing @imports. Make sure you add them in.

* `_index.scss`
* `_schedule.scs`
* `_sessions.scss`
* `_speakers.scss`
* `_about.scss`
* `_video.scss`












