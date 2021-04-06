# Read: 04 - HTML Links, CSS Layout, JS Functions
## HTML
+ Links:
`<li><a href="http://www.empireonline.com">Empire</a></li>` Linking to Other Sites

`<li><a href="index.html">Home</a></li>` Linking to Other Pages on the Sa me Site

   * Relative Link Type:

`<a href="reviews.html">Reviews</a>`  Same Folder 

 `<a href="music/listings.html">Listings</a>` Child Folder
 
  `<a href="movies/dvd/reviews.html"> Reviews</a>` Grandchild Folder
  
 `<a href="../index.html">Home</a>` Parent Folder
 
 `<a href="../../index.html">Home</a>` GrandParent Folder
 
   * Email Links:
 
    mailto: `<a href="mailto:jon@example.org">Email Jon</a>`
    
   * Opening Links in a New Window:
 
     target: `<a href="http://www.imdb.com" target="_blank"> Internet Movie Database</a> (opens in new window)`
     
   * Linking to a Specific Part of Another Page  
     ```
     <h1 id="top">Film-Making Terms</h1>
     <a href="#arc_shot">Arc Shot</a><br />
     ```
  + Layout:
    * positioning schemes:
       1. Normal flow: each item to appear lower down the page `position:static`
       2. Relative Positioning: shifting it to the top, right, bottom, or left of where it `position:relative`
       3. Absolute positioning: ignore the space it would have taken up, top right, and the paragraphs start at the top of the screen `position:absolute`
       4. Fixed Positioning:stays in the exact same place. `position:fixed` 
       5. Floating Elements : `float: right;`
       6. `clear: left;`
       7. Overflapping elements: `z-index`

      
   ## Javascript
   * Functions, Methods, and Objects” 
     
     
     
