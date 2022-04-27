# challenge-1
To refactor an existing webpage to make it accessible as to optimize the search engine.  It is also to restructure the format to have the code follow smoothly while following this image:
![](.assets/images/challenge-1-structure-image.png)

User Story
AS A marketing agency
-I WANT a codebase that follows accessibility standards
-SO THAT our own site is optimized for search engines


Acceptance Criteria
-GIVEN a webpage meets accessibility standards
-WHEN I view the source code
-THEN I find semantic HTML elements
-WHEN I view the structure of the HTML elements
-THEN I find that the elements follow a logical structure independent of styling and positioning
-WHEN I view the image elements
-THEN I find accessible alt attributes
-WHEN I view the heading attributes
-THEN they fall in sequential order
-WHEN I view the title element
-THEN I find a concise, descriptive title

## The Process
To make sure that the criteria is met, the following needs to be done:
-Understand the layout of the page and its purposes
-Research on the following to apply the code:
    -attributes located in the elements
    -Semantic HTML
    -a logical structure indepedent of styling and positioning
    -alt attribute
    -follow the sequential order

## The Structure

Screenshot on what we need to do:
![Website OVerall](https://github.com/elopez08/challenge-1/blob/main/assets/images/challenge-1-structure-image.png)

Follow the structure that is found within the code:

```
Structure of the comments were added in the:

<!-- Header -->

<!-- Section -->

<!-- Section -->

<!-- Aside -->

<!-- Footer -->

Change the title to "Horiseon Home Page"

Change the <div> to <header> in the header (located in the body)

Change the <div> to <section> with the class "hero" and "content"

On the <section> with the element content, change the <div> to <article>

Change the <div> to <aside> with the class "benefits"

Change <div> to <footer> on the final section located at the bottom

On the section with aside, change the h3 to h2 (do this also in the css where it is being identified)

Have an "alt" tag with each of the images

```


With that done, go to the CSS file to modify.

## Global Values

/* Univsersal Selector */
* {
    box-sizing: border-box;
    padding: 0;
    margin: 0;
}

With this, by default, all of the values will be shaped into that.  It'll have a border-box, a padding of 0, and it will have no margin.  This will be applied on everything (unless it is overwritten on the code that we instruct it to do).

I also included the following:

body {
    background-color: #d9dcd6;
}

/* Found throughout the code on specific elements: */

a {
    color: var(--main-white-color);
    text-decoration: none;
}

p {
    font-size: 16px;
}

Unlike the previous, this will not set the values to everything.  HOWEVER, should the element contain the value that is stated, then it will add those styles in the site.  For example, the "p" is the paragraph.  It doesn't matter if it is located in the body or in the header.  As long as it is being called "p", it will set the values initially as a font-size equal to 16px.  The only time this will be changed, like the last one, is when the value is rewritten.  This is because the last declaration that is being declared on the CSS will be the latest for it.

## Structural Content Layout

The structural format will have the following:


/* ======= Header ======= */
![Headedr Style](https://github.com/elopez08/challenge-1/blob/main/assets/images/header-section.png)


/* ======= Section ======= */
![Picture Section](https://github.com/elopez08/challenge-1/blob/main/assets/images/picture-section.png)


/* ======= Section ======= */
![Multiple Box Section](https://github.com/elopez08/challenge-1/blob/main/assets/images/box-section.png)


/* ======= Aside ======= */
![Aside Section](https://github.com/elopez08/challenge-1/blob/main/assets/images/aside-section.png)


/* ======= Footer ======= */
![Footer Section](https://github.com/elopez08/challenge-1/blob/main/assets/images/footer-section.png)


The pictures contains all the sections we're going to have on the page.  This is how we determine on the plan on making a design.

They were ordered to have it flow on the format of the HTML.  First it'll be the element rule first to identify the global, then the class selectors, then it'll follow the id selector

## The CSS Coding Structure

In addition to this, there were a few that were identified as :root to simplify the code further.  Here's the code:

:root {
    --main-white-color: #ffffff; /*use:  var(--main-white-color); */
    --font-family-one: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif; /*use: var(--font-family-one); */
    --display-inline: inline-block; /*use: var(--display-inline); */

}

With this, I can apply the code immediately by changing this line only.  For example, say, if I wanted to change white to black, I can do so with the --main-white-color by changing its attribute (at that point, though, renaming it would be a wise idea as well).

After declaring the root for simplification, we'll move on to the sections of the code.

## Header Style

The following is used for the style of the header:

The overall value of the header:
header {
    padding: 20px;
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
    background-color: #2a607c;
    color: var(--main-white-color);
}

When H1 is being declared within the header:
header h1 {
    display: var(--display-inline);
    font-size: 48px;
}

When H1 is being declared in the header while also having a class within the header as "seo"
header h1 .seo {
    color: #d9dcd6;
}

When the element "nav" is being called within the header:
header nav {
    padding-top: 15px;
    margin-right: 20px;
    float: right;
    font-family: var(--font-family-one);
    font-size: 20px;
}

When the element "ul" is being declared that's inside the "nav" while inside the "header"
header nav ul {
    list-style-type: none;
}

When the element "li" is being declared while it's inside "ul", which is also part of the "nav" and also is inside the "header":
header nav ul li {
    display: var(--display-inline);
    margin-left: 25px;
}

## Picture Section Style

The value of this section is:
.hero {
    height: 800px;
    width: 100%;
    margin-bottom: 25px;
    background-image: url("../images/digital-marketing-meeting.jpg");
    background-size: cover;
    background-position: center;
}

This is all we need for this section since it is just a picture.

## Multiple Box Section

The overall value that has this div is this:

.content {
    width: 75%;
    display: var(--display-inline);
    margin-left: 20px;
}

What this means is that EVERYTHING that's inside this div will be structured as this size.  Should we declare the values of the other "div"s to be 100%, it'll match the size that is being declared here, which is 75%.  Also, this will have a margin-left of 20px, meaning that it'll have a spacing on the left side.  Should there be no margin declaration on the other "div"s in this section, it'll still have it with respect to this code.

Next are the boxes:

There are groupings that were established.  Here are the following:

The declaration of the overall "div" (meaning the box sections):
.search-engine-optimization , .online-reputation-management , .social-media-marketing {
    margin-bottom: 20px;
    padding: 50px;
    height: 300px;
    font-family: var(--font-family-one);
    background-color: #0072bb;
    color: var(--main-white-color);
}

When we are in the class that's being declared, the "img" element that's inside will have the following:
.search-engine-optimization img , .online-reputation-management img , .social-media-marketing img {
    max-height: 200px;
}

Element "h2" will have its values defined as long as it is within the three classes:
.search-engine-optimization h2 , .online-reputation-management h2 , .social-media-marketing h2 {
    margin-bottom: 20px;
    font-size: 36px;
}

When I mentioned groupings, I meant the codes that have more than one class that has the same structure.  For example, 

.search-engine-optimization , .online-reputation-management , .social-media-marketing 

This means that the properties with the class "search-engine-optimization" will be the same if there's a class name of "online-reputation-management" and "social-media-marketing".  This is to condensed the coding overall so it looks simplier and easier to follow

We're going to do the same thing for the next section.

## Benefit (Aside) Section

The following values will be declared:

.benefit-lead , .benefit-brand , .benefit-cost {
    margin-bottom: 32px;
    color: var(--main-white-color);
}

.benefit-lead h2 , .benefit-brand h2 , .benefit-cost h2 {
    margin-bottom: 10px;
    text-align: center;
}

.benefit-lead img , .benefit-brand img ,  .benefit-cost img {
    display: block;
    margin: 10px auto;
    max-width: 150px;
}



## The Output

With the research, we were able to shorten the code, follow the structure more fluently, and have it set to follow the rules.  Comments on each section will also make easier to read on the project as well
as having the old format in case it needs to be refered back as a reference.  Should the comment be accepted and the code valid, it will be used to replace the code, effectively, shortening the overall code for both the css and html

## The Challenge

One of the biggest challenges is the code itself.  While we were given on what the code does and what the structure is like, it's backtracking that could prove to be a bit of a challenge.  How this was handled was not only using the inspect tool from Google Chrome, but also finding out where specifically the code resides and what changes needed to be made.

This is especially true with the code that was provided as default.  Originally, there were too many indent errors and too many divs to track.  Even though structurally it functioned correctly, the probelm is that when we want to edit the code back, it is really difficult at first glance.  I needed to find out where the brackets end and then give the proper indention so that I can go back to it without much of a problem.  Then, it's simply changing the "div"s to a more fitting name so I can see the structure better.

This process also taught me that would be crucial to the group projects since I'm not the only one that would be working on it.  I will be paired with multiple people for it to work.  On that note, it is important to leave comments and make the structure look as neat as possible so the others can read it and apply the necessary changes.