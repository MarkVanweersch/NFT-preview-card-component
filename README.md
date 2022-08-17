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

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover states for interactive elements

### Screenshot

- Mobile

![](/solution/mobile.png)

- Desktop

![](/solution/desktop.png)

- Desktop hover on image

![](/solution/desktop-active-1.png)

- Desktop hover on title

![](/solution/desktop-active-2.png)

- Desktop hover on author name

![](/solution/desktop-active-3.png)

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

### Built with

- CSS Flexbox
- Position absolute
- CSS Custom Properties

### What I learned

To overlay containers over one another and that some properties of a parent have effect on the properties of the child. To get the background of the image on hover to be opaque, I made the whole element opaque, which made the icon what appears on hover opaque too. Instead it was better to just make the background color opaque using an alpha value.

This is my css code to make the hover effect on the image:

```css
.img-container .view-icon-container {
  position: absolute;
  inset: 0;
  border-radius: 0.5em;
}

.img-container .view-icon-container:hover{
  background-color: var(--clr-primary-2-alpha);
}

.img-container .view-icon {
  visibility: hidden;
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
}

.img-container .view-icon-container:hover .view-icon {
  visibility: visible;
}
```

### Useful resources

- [w3schools.com](https://www.w3schools.com/howto/howto_css_display_element_hover.asp) - This helped me understand the css selectors better. Understanding how you can chage the value of one class while hovering over another. I use w3schools.com for almost all of my information and learning.