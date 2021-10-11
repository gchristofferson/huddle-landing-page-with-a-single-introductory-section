# Frontend Mentor - Huddle landing page with single introductory section solution

This is a solution to the [Huddle landing page with single introductory section challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/huddle-landing-page-with-a-single-introductory-section-B_2Wvxgi0). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
    - [The challenge](#the-challenge)
    - [Screenshot](#screenshot)
    - [Links](#links)
- [My process](#my-process)
    - [Built with](#built-with)
    - [What I learned](#what-i-learned)
- [Author](#author)


## Overview

### The challenge

Users should be able to:

- View the optimal layout for the page depending on their device's screen size
- See hover states for all interactive elements on the page

### Screenshot

![](./images/screenshot.jpg)


### Links

- Solution URL: [https://github.com/gchristofferson/huddle-landing-page-with-a-single-introductory-section](https://github.com/gchristofferson/huddle-landing-page-with-a-single-introductory-section)
- Live Site URL: [https://gchristofferson.github.io/huddle-landing-page-with-a-single-introductory-section/](https://gchristofferson.github.io/huddle-landing-page-with-a-single-introductory-section/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Mobile-first workflow

### What I learned

In this project I got more practice with Flexbox which I have been using consistently in most of my layouts lately.  Something new though that I have also started to incorporate into my projects is the use of the `transition` property to move elements.  Before I would use a lot of relative or absolute positioning.  I'm so glad I discovered `transition` because it makes positioning elements a breeze.  In this project I used it in two specific areas where I was having trouble matching the design.  

The first area was the `.hero-content` div element.  On the parent `.container` I set `display: flex` and `align-items: center`.  At the desktop layout (1440px), this got the alignment of the `.hero-img-container` and the `.hero-content` in the ballpark of the design.  However, to get it as close to pixel perfect as I could, I decided to use `transform: translateY()` on the `.hero-content` div to nudge it up a few pixels.  This result matched the design much more closely.

Here is the `.hero-content` flex container with the hero image and content I was trying to perfectly align:

```html
<main class="main container">

  <div class="hero-img-container">
    <img src="./images/illustration-mockups.svg" alt="mockups illustration" class="hero-img">
  </div>

  <div class="hero-content">
    <h1 class="hero-content__title">Build The Community Your Fans Will Love</h1>
    <p class="hero-content__text">Huddle re-imagines the way we build communities. You have a voice, but so does your audience.
      Create connections with your users as you engage in genuine discussion. </p>
    <button class="hero-content__btn">Register</button>
  </div>

</main>

```
Here's the css I used to align them to match as closely to the design as possible using a combination of flex align-items on the parent and transform on the `.hero-content` container:

```css
.container {
  display: flex;
  flex-direction: row;
  align-items: center;
  max-width: 1440px;
}

.hero-img-container {
  margin-bottom: 0;
  width: 55%;
}

.hero-img {
  min-width: 100%;
}

.hero-content {
  margin-bottom: 27px;
  width: 40%;
  transform: translateY(-35px);
}

```

## Author

- Frontend Mentor - [@gchristofferson](https://www.frontendmentor.io/profile/gchristofferson)
- Twitter - [@GreggChristoff2](https://twitter.com/GreggChristoff2)
