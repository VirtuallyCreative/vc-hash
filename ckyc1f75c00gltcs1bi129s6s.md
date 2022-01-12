## Introduction to LESS - Part 2


## Using LESS #2: Nested Rules

This is something I love using when marking up CSS with LESS. Rather than constructing long selector names to specify inheritance, in LESS you can simply nest selectors inside other selectors. This makes inheritance from parents much easier to visualize on a page, at least in my opinion. Check this out, this is how you should normally go about styling the paragraph in our header HTML markup:

```css
#header h2 { font-size: 26px; font-weight: bold; } 
#header p { font-size: 12px; color: #FFFFFF; } 
#header p a { text-decoration: none; } 
#header p a:hover { border-width: 1px; } 
```

Ok nothing new here. If you wanted to target children, you have to declare the parent first, then each child element till you arrive at the one you want to style. Boring!! With Nested Rules you can write Example 2 like this:

```less
// LESS

#header {
 
    h2 { 
        font-size: 26px; 
        font-weight: bold; 
    } //Close h2 
    
    p { 
        font-size: 12px; 
        color: @color; 
        
        a { 
            text-decoration: none; 
                
            &:hover { 
                    border-width: 1px; 
           } // Close :hover 
       
        } // Close a 
   
    } // Close p 

} // Close #header 
```

Now, when you "nest" a child element inside its parent, it takes all the styling of the parent and applies it to the children for you! Notice the `&` combinator. It is used when you want a nested selector to be concatenated (joined) to its parent selector, instead of acting as a descendent. This is especially important for pseudo-classes like `:hover` and `:focus`. I'll wait a second while you calm yourself from the realization of how much time you could of saved yourself on past projects using this method.

## Using LESS #3: Mixins (Parametric Included)

If you're like me and other developers/designers and want your fancy CSS 3 shadows, rounded borders etc... working on all browsers you know the pain of typing out all the versions for each runtime (moz, webkit, standard) so this is where Mix-In's come into play. **Mixins allow you to embed all the properties of a class into another class by simply including the class name as one of its properties!** Yes, I realize that sounds like a mouthful, but think of it like a variable, but for whole CSS classes. **Mixins can also behave like functions too and take arguments as well**, as seen below in Example 3:

```less
// LESS

@footcolor: #000000;

// Create Mixin .rounded-corners and assign a @radius: variable to pass through

.rounded-corners (@radius: 5px) { 
        border-radius: @radius; 
        -webkit-border-radius: @radius; 
        -moz-border-radius: @radius; 
}

#header { .rounded-corners; } 

#footer { 
    background-color: @footcolor; 
    .rounded-corners(10px); 
}
```

```css
/* Compiled CSS in browser */

#header { 
    border-radius: 5px; /* This is 5px because that's the default @radius value we set */ 
    -webkit-border-radius: 5px; /* This is 5px because that's the default @radius value we set */ 
    -moz-border-radius: 5px; /* This is 5px because that's the default @radius value we set \*/ 
} 

#footer { 
    background-color: #000000; 
    border-radius: 10px; /* This is 10px because we passed a value of 10px */ 
    -webkit-border-radius: 10px; /* This is 10px because we passed a value of 10px */ 
    -moz-border-radius: 10px; /* This is 10px because we passed a value of 10px */ 
}
```

Wow lots going on here so let's break Example 3 down! The proper usage to make a Mixin is like a CSS class and Javascript function in one. Proper usage is `.mixinName() {}`. Looking like a CSS class but, has the power of a Javascript function.

So we want to set a border-radius but only want to type out the code once. We can set a mixin to call all 3 at the same time by making one like a variable but rather than give it one value, we can assign multiple to a mixin:

```less
//LESS

.rounded-corners() { 
    border-radius: 5px; 
    -webkit-border-radius: 5px; 
    -moz-border-radius: 5px; 
}

#header { .rounded corners; }
```

So here we made our mixin and gave it something to output. And this would work for our Example 3 /\* Compiled CSS in Browser \*/ result for `#header` but we want more control over the border-radius and we don't want to make a different mixin for each different radius size so we can give the mixin an argumen to pass through to our styling:

```less
//LESS

.rounded-corners(@radius: 5px;) { 

// 1) We create our new variable inside the Mixin border-radius: 
@radius; 

// 2) We then Add the Variable where it needs to appear to affect the styling -webkit-border-radius: @radius; 
-moz-border-raidus: @radius; }

#footer { 
    background-color: @footcolor; 
    .rounded-corners(10px); 
}
```

Now we have a Parametric Mixin! This would output the `#footer` result from Example 3 /\* Compiled CSS in Browser \*/ above. Bypassing the `10px` as the mixin's argument you can effectively alter the created variable to your liking! You will use Mixins often if you choose to use LESS so this concept is particularly important. Try it out and play around with them to learn how they work.