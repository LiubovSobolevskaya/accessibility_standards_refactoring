# Accessibility Standards Refactoring


[The link to the deployed page](https://liubovsobolevskaya.github.io/accessibility_standards_refactoring/#social-media-marketing)
______________


This is the challenge for the first week of the UCB Bootcamp, where we will be working on improving an existing HTML and CSS document to comply with accessibility standards. The goal is to ensure that the changes made do not affect the visual appearance of the page.

## Learning Points 
In this challenge, we aim to address the following questions:

* What are accessibility standards and why are they important?
* What are semantic HTML elements?
* What is an accessible alt attribute?
* What are heading attributes and what sequential order do they fall in?
* What is a title element and what is it intended to describe?

## Technology Used 

* [HTML](https://developer.mozilla.org/en-US/docs/Web/HTML)
* [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS)      
* [Git](https://git-scm.com/)       


## Mock-Up

Here is the web application's appearance and functionality:
![The Horiseon webpage includes a navigation bar, a header image, and cards with text and images at the bottom of the page.](./assets/readme_img/01-html-css-git-homework-demo.gif)

## Code Refactor Example

I changed the following code:
```html
<div class="content">
    <div class="search-engine-optimization">
        <img src="./assets/images/search-engine-optimization.jpg" class="float-left" />
        <h2>Search Engine Optimization</h2>
        <p>
            The dominance of mobile internet use means that users are searching for the right business as they travel, shop, or sit on their couch at home. Search Engine Optimization (SEO) allows you to increase your visibility and find the right customers for your business.
        </p>
    </div>
    <div id="online-reputation-management" class="online-reputation-management">
        <img src="./assets/images/online-reputation-management.jpg" class="float-right" />
        <h2>Online Reputation Management</h2>
        <p>
            The web is full of opinions, and some of these can be negative. Social media allows anyone with an internet connection to say whatever they want about your business. Online Reputation Management gives you the control over what potential customers see when they search for your business.
        </p>
    </div>
    <div id="social-media-marketing" class="social-media-marketing">
        <img src="./assets/images/social-media-marketing.jpg" class="float-left" />
        <h2>Social Media Marketing</h2>
        <p>
            Social media continues to have a sizable influence on buying habits. Social media marketing helps you determine which platforms are suited to your brand, using analytics to find the right markets and increase your lead generation.
        </p>
    </div>
</div>

```
to:

```html
<main class='content'>
    <section id='search-engine-optimization' class='content-card'>
        <img src='./assets/images/search-engine-optimization.jpg' class='float-left' alt = 'laptop with a magnifying glass on it, a notebook with an abbreviation SEO and related terms written on it, a cup with a coffee, and pens'/>
        <h2>Search Engine Optimization</h2>
        <p>
            The dominance of mobile internet use means that users are searching for the right business as they travel, shop, or sit on their couch at home. Search Engine Optimization (SEO) allows you to increase your visibility and find the right customers for your business.
        </p>
    </section>
    <section id='online-reputation-management' class='content-card'>
        <img src='./assets/images/online-reputation-management.jpg' class='float-right' alt = 'partial view of a person holding a mobile phone and working on a laptop with a word REPUTATION and several charts on the screen' />
        <h2>Online Reputation Management</h2>
        <p>
            The web is full of opinions, and some of these can be negative. Social media allows anyone with an internet connection to say whatever they want about your business. Online Reputation Management gives you the control over what potential customers see when they search for your business.
        </p>
    </section>
    <section id='social-media-marketing' class='content-card'>
        <img src='./assets/images/social-media-marketing.jpg' class='float-left'  alt = 'six people sitting behind a table with several devices and vivid stickers with internet-related pictures and words on top of the table'/>
        <h2>Social Media Marketing</h2>
        <p>
            Social media continues to have a sizable influence on buying habits. Social media marketing helps you determine which platforms are suited to your brand, using analytics to find the right markets and increase your lead generation.
        </p>
    </section>       
</main>
```
Here I converted the above non-semantic <div\> with the class of "content" to an appropriate <main\>  semantic element. I also added alt attribute to improve accessibility. Additionally, I changed different class names to the same class name, to avoid redundancy it the the corresponding style.css file:

```css
.content {
    width: 75%;
    display: inline-block;
    margin-left: 20px;
}
.search-engine-optimization {
    margin-bottom: 20px;
    padding: 50px;
    height: 300px;
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    background-color: #0072bb;
    color: #ffffff;
}

.online-reputation-management {
    margin-bottom: 20px;
    padding: 50px;
    height: 300px;
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    background-color: #0072bb;
    color: #ffffff;
}

.social-media-marketing {
    margin-bottom: 20px;
    padding: 50px;
    height: 300px;
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    background-color: #0072bb;
    color: #ffffff;
}

.search-engine-optimization img {
    max-height: 200px;
}

.online-reputation-management img {
    max-height: 200px;
}

.social-media-marketing img {
    max-height: 200px;
}

.search-engine-optimization h2 {
    margin-bottom: 20px;
    font-size: 36px;
}

.online-reputation-management h2 {
    margin-bottom: 20px;
    font-size: 36px;
}

.social-media-marketing h2 {
    margin-bottom: 20px;
    font-size: 36px;
}

```
to:
```css

.content {
    color: #ffffff;
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    width: 75%;
    display: inline-block;
    margin-left: 20px;
}

.content-card{
    margin-bottom: 20px;
    padding: 50px;
    height: 300px;
    background-color: #0072bb;
}

.content-card img {
    max-height: 200px;
}

.content-card h2 {
    margin-bottom: 20px;
    font-size: 36px;
}
```

## Author Info

### Liubov Sobolevkaya
* [LinkedIn](https://www.linkedin.com/in/liubov-sobolevskaya-45756a101/)
* [Github](https://github.com/LiubovSobolevskaya)
* [Kaggle](https://www.kaggle.com/lyubovsobolevskaya)

