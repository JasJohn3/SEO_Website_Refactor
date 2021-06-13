# SEO Website Refactor

## Code Optimization for Accessibility

The Purpose of this exercise is to demonstrate how to refactor existing code to modern HTML5 elements and increase access to those with disabilities.  Through out the project, most of the original code is commented out for demonstration purposes only to highlight the changes made during the exercise.  These comments can be removed at anytime to make the code more readible.

## Feature Changes & Highlights

This segment will include a list of the more prominent changes to increase accessibility.

### `<header>` and `<nav>` elements
This segment shows the use of the `<header>` and `<nav>` elements to create our navbar commonly found on most websites.
  ``` 
      <header>
        <h1>Hori<span class="seo">seo</span>n</h1>
        <!-- Modified div to nav and adjusted css references to reflect nav -->
        <nav>
            <ul>
                <li>
                    <a href="#search-engine-optimization">Search Engine Optimization</a>
                </li>
                <li>
                    <a href="#online-reputation-management">Online Reputation Management</a>
                </li>
                <li>
                    <a href="#social-media-marketing">Social Media Marketing</a>
                </li>
            </ul>
        </nav>
    </header>
  ```
### `<section>` and `<article>` elements
The `<div>` elements that were originally used were replaced with `<section>` and `<article>`.  This allows screen readers to identify these elements separately and also provide the ability to use css element selectors in place of class names.
``` 
        <section class="benefits">
        <!-- modified div to be article -->
        <article class="benefit-styling">
            <h3>Lead Generation</h3>
            <img src="./assets/images/lead-generation.png" />
            <p>
                Inbound strategies for lead generation require less work for your business, bringing customers directly to your website.
            </p>
        </article>
        <!-- modified div to be article -->
        <article class="benefit-styling">
            <h3>Brand Awareness</h3>
            <img src="./assets/images/brand-awareness.png" />
            <p>
                Users find your business through paid and organic searches, increasing the search ranking and visibility for your business.
            </p>
        </article>
        <!-- modified div to be article -->
        <article class="benefit-styling">
            <h3>Cost Management</h3>
            <img src="./assets/images/cost-management.png"></img>
            <p>
                As the search ranking for your business increases, your advertising costs decrease, and you no longer need to advertise your page.
            </p>
        </article>
    </section>
```
### `<footer>` element
The `<footer>` element replaced the original `<div>`.
``` 
      <footer>
        <h2>Made with ❤️️ by Horiseon</h2>
        <p>
            &copy; 2019 Horiseon Social Solution Services, Inc.
        </p>
    </footer>
```

### Jumbotron/Hero image
The Jumbotron is one of the major highlight features for accessibility.  Initially, the jumbotron was a `<div class="hero">`.  This was changed to
    ```  
        <section ><img src="./assets/images/digital-marketing-meeting.jpg" alt="Four people gather around for an office meeting reviewing documents" class="hero"></section>
    ```
This modification allows screen readers to be able to read the alt attribute of the image.  Addtionally, the css was modified to exclude the background image and the original `<div>` was changed to a `<section>`

### `<main>` element
The `<main>` element was changed from a `<div class="content">`.  This allows for our content to have separation as well as giving the screen reader the ability to define where the main content of the page is located.

## CSS Optimization

### Refactoring repetive CSS code with Element Selectors and Class Names

There were many areas in witch identical css code was applied to html elements when a single class name would be able to replace these styling options. That reduces the total amount of css code required to style the page.  Here is an example including the original code that was commented out.
```
/* created new class benefits-styling for universal styling of html elements */
.benefit-styling{
    margin-bottom: 32px;
    color: #ffffff; 
}
/*              Redundant CSS CODE                          */
/* .benefit-lead {
    margin-bottom: 32px;
    color: #ffffff;
}

.benefit-brand {
    margin-bottom: 32px;
    color: #ffffff;
}

.benefit-cost {
    margin-bottom: 32px;
    color: #ffffff;
} */
/*              Redundant CSS CODE                          */
```
Here is an example of where css element selectors can be used in place of class names.  In this example code, the `<header>` and `<nav>` elements are used as css selectors to ensure no other `<ul>` or `<li>` element is targeted on the page.  This demonstrates the value of using modern HTML5 elements.
```
/* changed class ="header" to be HTML Element header and modified div to be nav */
header nav ul {
    list-style-type: none;
}
/* changed class ="header" to be HTML Element header*/
header  ul li {
    display: inline-block;
    margin-left: 25px;
}
```
## Conclusion
Overall this is a valuable exercise that demonstrates the applicability of modern HTML5.  Through the use of HTML5 elements, we have more options to use in our CSS and web design.  This increases accessibilty and allows for more readable code as well.