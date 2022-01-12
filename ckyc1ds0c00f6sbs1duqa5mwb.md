## Introduction to LESS - Part 1


## The Dynamic Style-sheet Language

Hope you guys find this brief introduction useful, as I know this has changed the way I use CSS forever!

What this tutorial is covering today is how to add variables, mixins, nested rules and much more to CSS 3 to make it function like you have never seen before! The amount of benefits you can gain from being able to optimize your CSS could be explained here but I just won't do it justice until you see it in action. It should take you about 1 hour to learn the concepts presented here.

This tutorial already assumes you know how to code (X)HTML and CSS 3 and should be comfortable with creating basic layouts of pages (including header, content, sidebars, footers and can style individual elements within containers and it's children). 

Knowledge of:

- Grouping/Nesting
- Dimensions
- Display
- Positioning
- Floating
- Align
- Pseudo-class
- Pseudo-element
- Image Opacities
- Image Sprites
- Media Types
- CSS Attribute Selectors

would be a big help, but not required. However, I won't be covering (X)HTML/CSS itself in this tutorial, just possibly using elements within those topics, so if you're unfamiliar with them I suggest you do a little reading up! If you're unable to write CSS mark-up "on-the-fly" that's not a big deal but, you might want have a stronger base before you start manipulating it! I know I confused myself with my own projects sometimes so making a strong foundation correctly to build upon will always serve you well in the future.

I know what you're thinking now.. "Wait a minute! You can't add variables and all this "mix-in stuff" to CSS! So what's going on here!?".

Well you're correct! Cascading Style Sheets doesn't support this style of scripting but when we add a very clever Javascript libary called LESS.js we can expand CSS beyond just its normal capabilities. Check this out:

```less
// LESS 
@color: #FFFFFF; 

#header { 
    background-color: #000000; 
} 

h2 { color: @color; } 

/* Compiled CSS in browser */ 
#header { background-color: #000000; } 
h2 { color: #FFFFFF; }
```

That is LESS in action with CSS. If you already grasp the concept outlined above then you're well on your way to seeing how powerful LESS is and will help in day-to-day CSS coding.

If you already use LESS in your CSS projects then please let us know how you use it to your advantage and some of the things you've created!

#### LESS Info:

LESS was developed by [Alexis Sellier](http://cloudhead.io/ "Alexis Sellier"), more commonly known as [cloudhead](http://cloudhead.io/ "cloudhead"). I am in no way or part taking credit for LESS obviously, just showing you some really cool ways to use it in your CSS coding. You can read more information, see some of the tutorial examples and learn more about LESS.js on the [official page](http://lesscss.org/ "External link").

### Let's begin: LESS Setup

To achieve what we did with that `#header` and `h2` property above, a couple of steps are needed. First we need to setup our environment to use LESS within CSS. This is very easy and can be done in a few steps.

**Step 1:** 
Add it to your project locally in development or, add the two LESS files (`.css` and `.js`) to your client-side page! 


Use with Node.js:

```bash
npm install -g less
lessc styles.less styles.css
```

Or the browser:
```html
<link rel="stylesheet/less" type="text/css" href="styles.less" />
<script src="https://cdn.jsdelivr.net/npm/less@4.1.1" ></script>
```

If you noticed, the `rel="stylesheet/less"` and the `href="styles.less"` are different than the normal `"stylesheet/css"` and `styles.css` respectively. In our case LESS uses a special stylesheet ending (.less) which it parses and then outputs a live stylesheet for the browser. Nifty huh! So that means our default stylesheet has a .less ending hence the `"stylesheet/less"` relationship. 

Now we can start using style.less to style our web page like normal!

### Using LESS #1: Variables

Our first topic is Variables. If you've ever used Javascript, PHP or any other larger scripting language sooner rather than later, you'll run into variables.

For our purpose, variables allow you to specify widely used values in a single place, and then re-use them throughout the stylesheet. This makes global changes as easy as changing one line of code! Lets use Example 1 and break it down.

Inside our style.less we can define a variable by using the @ symbol before the desired variable name and then give it any value we want. Then we call the variable inside the CSS property #header:

```less
@color: #FFFFFF;

#header { color: @color; }
```

Here we made a new variable `@color:` and its value set to `#FFFFFF`. To use this new variable we made, we are going to assign it to `color:` by replacing the spot the colour hex number (#FFFFFF) normally would have gone. If you save and refresh the page in a browser and view your CSS (I love Firebug for Firefox, or Inspect Element in Safari/Chrome) you should see:

```css
#header { color: #FFFFFF; }
```

This means it works! You just successfully made your first CSS variable using LESS.js!

So back to Example 1, it's the same concept just with more than one use. That's the beauty of variables! You can use them over and over and it can save you lots of time when you have different specific colours for specific links, nav elements, box shadows etc... but note that variables are actually ‘constants’ in that they can only be defined once. 

I'll let you play around with the idea and when you're comfortable with creating multiple variables and calling them in various properties we can move on.