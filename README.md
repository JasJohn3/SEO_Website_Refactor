# SEO Website Refactor

## Code optimization for Accessibility

The Purpose of this exercise is to demonstrate how to refactor existing code to modern HTML5 elements and increase access to those with disabilities.  Through out the project, most of the original code is commented out for demonstration purposes only to highlight the changes made during the exercise.  These comments can be removed at anytime to make the code more readible.

## Feature Changes Highlights

This segment will include a list of the more prominent changes to increase accessibility.

## `<header>` and `<nav>` elements
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
##`<section>` and `<article>` elements
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
## `<footer>` element
``` 
      <footer>
        <h2>Made with ❤️️ by Horiseon</h2>
        <p>
            &copy; 2019 Horiseon Social Solution Services, Inc.
        </p>
    </footer>
```

## Jumbotron/Hero image
The Jumbotron is one of the major highlight features for accessibility.  Initially, the jumbotron was a <div class="hero">.  This was changed to
    ```  
        <section ><img src="./assets/images/digital-marketing-meeting.jpg" alt="Four people gather around for an office meeting reviewing documents" class="hero"></section>
    ```
This modification allows screen readers to be able to read the alt attribute of the image.  Addtionally, the css was modified to exclude the background image and the original `<div>` was changed to a `<section>`

## <main> element
The <main> element was changed from a <div class="content">
