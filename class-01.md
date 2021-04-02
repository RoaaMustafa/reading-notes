# Class-01 Code 201
## From the Duckett HTML book:

## 1. Introduction (pp.2-11)
* HTML is used to create web pages
* CSS uses rules to enable you to control the styling and layout of web pages
* When you ask your browser for a web page, the request is sent across the Internet to a special computer known as a web server which hosts the website.
* All websites use HTML and CSS, but content management systems, blogging software, and e-commerce platforms often add a few more technologies into the mix.

## 2. HTML Chapter 1: “Structure” (pp.12-39)
* HTML pages are text documents.
* HTML uses tags (characters that sit inside angled brackets) to give the information they surround special meaning.
* Tags are often referred to as elements.
* Tags usually come in pairs. The opening tag denotes the start of a piece of content; the closing tag denotes the end.
* Opening tags can carry attributes, which tell us more about the content of that element.
* Attributes require a name and a value.
* To learn HTML you need to know what tags are available for you to use, what they do, and where they can go.
<html>
<body>
<h1>This is the Main Heading</h1>
<p>This text might be an introduction to the rest of the page. And if the page is a long one it might be split up into several sub-headings.<p>
<h2>This is a Sub-Heading</h2>
<p>Many long articles have sub-headings so to help you follow the structure of what is being written. There may even be sub-sub-headings (or lower-level headings).</p>
<h2>Another Sub-Heading</h2>
<p>Here you can see another sub-heading.</p>
</body>
</html>

<html>
<head>
<title>This is the Title of the Page</title>
</head>
<body>
<h1>This is the Body of the Page</h1>
<p>Anything within the body of a web page is displayed in the main browser window.</p>
</body>
</html>

## 3. HTML Chapter 8: “Extra Markup” (p.176-199) 
* Comments in HTML <!-- comment goes here -->
* ID Attribute <p id="pullquote"></p>
* Class Attribute <p class="important"> </p>
* Block Elements :
<h1>Hiroshi Sugimoto</h1>
<p>The dates for the ORIGIN OF ART exhibition are as follows:</p>
<ul>
<li>Science: 21 Nov - 20 Feb 2010/11</li>
<li>Architecture: 6 Mar - 15 May 2011</li>
<li>History: 29 May - 21 Aug 2011</li>
<li>Religion: 28 Aug - 6 Nov 2011</li>
</ul>

* Inline Elements:Examples of inline elements are
<a>, <b>, <em>, and <img>.

* Grouping Text & Elements In a Block: <div id="header"> </div> "The <div> element allows you to
group a set of elements together in one block-level box. "
* Grouping Text & Elements Inline: <span class="gallery">Tate Modern</span>
* <iframe> : src, width, height, scrolling, frameborder, seamless
<iframe
width="450"
height="350"
src="http://maps.google.co.uk/maps?q=moma+new+york
&amp;output=embed">
</iframe>

* <meta> : The <meta> element lives inside the <head> element and contains information about that web page.
 description, keywords, robots, author, pragma, expires, 
 * There are some characters that are used in and reserved by HTML code.
![Characters](/code201/characters.JPG)

## 4. HTML Chapter 17: “HTML5 Layout” (pp.428-451)
* The <header> and <footer> elements can be used for:
  - The main header or footer that appears at the top or bottom of every page on the site.
  - A header or footer for an individual <article> or <section> within the page.
* <nav> element is used to contain the major navigational blocks on the site such as the primary site navigation.  
* <article> element acts as a container for any section of a page that could stand alone and potentially be syndicated.
* <aside> element has two purposes, depending on whether it is inside an <article> element or not.
* <section> element groups related content together, and typically each section would have its own heading.
* <hgroup> element is to group together a set of one or more <h1> through <h6> elements so that they are treated as one single heading.
* <figure>
<img src="images/bok-choi.jpg" alt="Bok Choi" />
<figcaption>Bok Choi</figcaption>
</figure>


## 5. HTML Chapter 18: “Process & Design” (pp.452-475)
* It's important to understand w XX ho your target audience is, why they would come to your site, what information they want to find and when they are likely to return.
* Site maps allow you to plan the structure of a site.
* Wireframes allow you to organize the information that will need to go on each page.
* Design is about communication. Visual hierarchy helps visitors understand what you are trying to tell them.
* You can differentiate between pieces of information using size, color, and style.
* You can use grouping and similarity to help simplify the information you present.

