# Understanding the Browser Rendering Pipeline

I wanted to know **how things actually work on the web**, so I started digging into the under the hood stuff.  

This is a little space where I’m documenting what I learned about the **browser rendering pipeline**. If you’re someone who likes understanding the fundamentals rather than just memorizing syntax, this might help you.  

--------------------


See, Whenever something changes on a web page like JavaScript updating text, CSS changing colors, or an image loading, the browser has to **turn code into pixels on your screen**.  

That whole process is called the **rendering pipeline** , that's it !! 

-------------------

## The Steps (In Simple Words)

Here’s what happens behind the scenes, step by step:  

**1) JavaScript Execution**  
- The browser runs your JS code.  
- This might touch the DOM, change styles, or manipulate data.  

**2) Style Calculation**  
- The browser figures out **what each element should look like**: colors, sizes, fonts, etc.  
- Even a small change, like a button color, triggers this step.  

**3) Layout / Reflow**  
- The browser decides **where everything goes** on the page.  
- Measures positions, widths, heights, margins… everything.  
- This is called **layout** or **reflow**, and it can be expensive if many elements change.  

**4) Paint**  
- Now the browser **fills in pixels**: colors, borders, text, shadows.  
- This is where things actually start appearing visually.  

**5) Compositing**  
- Finally, the browser takes all painted layers and **composites them onto the screen**.  
- This is what you end up seeing smooth animations, updated content, everything in place.  

---------------------

## Why It Matters

- Every tiny change in the DOM can trigger this whole pipeline 😵.
- 
- Updating the DOM too often can **slow down your page**, make animations lag, or make scrolling janky.
-  
- This is exactly why frameworks like **React** try to **minimize direct DOM updates**:
- 
  - Work happens in **cheap JS objects first (Virtual DOM)**  
  - Compare what changed  
  - Apply **only minimal DOM updates**  


-------------




    JS Execution

     |
     
    Style Calculation
 
     |
     
    Layout
    
     |
     
    Paint
    
     |
     
    Compositing
 
     |
     
    Screen





------------------------------------








## Why I Made This Repo

I always used the DOM and wrote React apps without truly understanding **what happens when something updates on the screen**.  

Once I dug into browser internals and the rendering pipeline, everything started making sense.  

So I wrote this down in the **simplest way I could**.  

If you’re someone who:  

- Is learning React  
- Wants to understand rendering  
- Keeps hearing “DOM is slow but JS is fast”  
- Or enjoys going a bit deeper than tutorials  

…then this explanation might help you too.  

---

## Help Me Improve This

I’m still learning, so if I **missed something** or made a **mistake**, your contributions or feedback are more than welcome.  

Feel free to **explore, fork, or open issues** if you want something explained here. I’ll keep expanding this as I learn more ❤

## THANKYOU !


