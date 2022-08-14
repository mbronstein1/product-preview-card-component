# Frontend Mentor - Product preview card component solution

This is a solution to the [Product preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/product-preview-card-component-GO7UmttRfa). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)

## Overview
This solution from Frontend Mentor uses HTML and CSS in an attempt to replicate a pre-existing product preview card component from scratch. Flexbox and media queries were used to achieve correct positioning and responsiveness for multiple screens.

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover and focus states for interactive elements

### Links

- Solution URL: [https://www.frontendmentor.io/challenges/product-preview-card-component-GO7UmttRfa/hub/product-preview-card-component-using-html-css-flexbox-media-queries-fc2BuIDlMt](https://www.frontendmentor.io/challenges/product-preview-card-component-GO7UmttRfa/hub/product-preview-card-component-using-html-css-flexbox-media-queries-fc2BuIDlMt)
- Live Site URL: [https://mbronstein1.github.io/product-preview-card-component/](https://mbronstein1.github.io/product-preview-card-component/)

## My process
First, I organized the HTML into different sections, allowing for simple flexbox positioning later as I moved to the CSS. I developed the CSS with a mobile-first mindset, creating a media query to adjust the formatting of the card component as the screen gets bigger.

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Mobile-first workflow
- Media queries

### What I learned

One specific thing I learned while working on this solution is how to change images when adjusting the size of the screen with media queries. 

I included two different image elements w/ a class of "image1" and "image2" respectively. An ID would have also worked in this scenario because they were unique identifiers.
```html
<img class="image1" src="images/image-product-mobile.jpg" alt="product image">
<img class="image2" src="images/image-product-desktop.jpg" alt="product image">
```

Then in the main CSS section I included the following:
```css
.image1 {
    width: 100%;
    border-radius: 2% 2% 0 0;
}

.image2 {
    display: none;
}
```

Then I added a media query for viewports wider than 375px, and included the following:
```css
.image2 {
        display: block;
        width: 100%;
        border-radius: 2% 0 0 2%;
        object-fit: cover;
    }
    .image1 {
        display: none;
    }
```

### Continued development

I am still trying to get comfortable with responsiveness, especially as browsers get smaller. I was able to create the card component and allow it to react to the browser successfully as it gets larger, but when the browser got smaller, the items within the card would squeeze together but maintain their size, causing the card to get taller, eventually to the point where the browser would require a scroll bar to view the entire card. Also the image on the left of the card would get progressively more squished width-wise and massively distorted. I still have a lot to learn, but this was a fun and relatively easy challenge exploring simple elements of HTML and CSS.