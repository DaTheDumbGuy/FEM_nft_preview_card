# Frontend Mentor - NFT preview card component solution

This is a solution to the [NFT preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/nft-preview-card-component-SbdUL_w0U). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover states for interactive elements

### Screenshot

![](./screenshot.png)

### Links

- Live Site URL: [NFT Preview Card](https://dathedumbguy.github.io/FEM_nft_preview_card/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid(Used it once)
- Mobile-first workflow

### What I learned

Using ::before pseudo-element, I created an overlay which is currently hidden(opacity) and will only show once the user :hover on top of the Image container(.nft_img_container).

```css
.nft_header .nft_img_container::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: hsla(178, 100%, 50%, 0.5);
  background-image: url(../images/icon-view.svg);
  background-repeat: no-repeat;
  background-position: center;
  opacity: 0;
  border-radius: 10px;
  transition: opacity 0.3s ease;
}
.nft_header .nft_img_container:hover::before {
  cursor: pointer;
  opacity: 1; /* Show the overlay on hover */
}
```

To be honest this is the first time I use hover together with pseudo-element ::before. The process of execution is basically:

When the user hovers over the container, it targets the pseudo-element ::before, which has an opacity set to 1. This makes the ::before element visible until the user removes the hover effect.

### Useful resources

- [W3School](https://www.w3schools.com/) - This helped me when I forgot some syntax. I usually go here to check if I'm using the sytax correctly.

## Author

- Frontend Mentor - [@DaTheDumbGuy](https://www.frontendmentor.io/profile/DaTheDumbGuy)

- Facebook - [Daryl Bacurin](https://www.facebook.com/profile.php?id=100087293514427)
