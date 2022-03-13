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

\
With that done, go to the CSS file to modify:

/*

    Global and Element Rules

*/

/*

    Structural Content Format

*/

/* ======= Header ======= */

/* ======= Section ======= */

/* ======= Section ======= */

/* ======= Aside ======= */

/* ======= Footer ======= */

They were ordered to have it flow on the format of the HTML.  First it'll be the element rule first to identify the global, then the class selectors, then it'll follow the id selector

In addition to this, there were a few that were identified as :root to simplify the code further.  Here's the code:

:root {
    --main-white-color: #ffffff; /*use:  var(--main-white-color); */
    --font-family-one: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif; /*use: var(--font-family-one); */
    --display-inline: inline-block; /*use: var(--display-inline); */

}

There are groupings that were established.  Here are the following:

.search-engine-optimization , .online-reputation-management , .social-media-marketing {
    margin-bottom: 20px;
    padding: 50px;
    height: 300px;
    font-family: var(--font-family-one);
    background-color: #0072bb;
    color: var(--main-white-color);
}

.search-engine-optimization img , .online-reputation-management img , .social-media-marketing img {
    max-height: 200px;
}

.search-engine-optimization h2 , .online-reputation-management h2 , .social-media-marketing h2 {
    margin-bottom: 20px;
    font-size: 36px;
}

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

##The Output
With the research, we were able to shorten the code, follow the structure more fluently, and have it set to follow the rules.  Comments on each section will also make easier to read on the project as well
as having the old format in case it needs to be refered back as a reference.  Should the comment be accepted and the code valid, it will be used to replace the code, effectively, shortening the overall code for both the css and html