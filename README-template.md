# Frontend Mentor - Product preview card component solution

This is a solution to the [Product preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/product-preview-card-component-GO7UmttRfa). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover and focus states for interactive elements

### Screenshot

![Product Card Desktop View](./screenshot-desktop.png)
![Product Card Mobile View](./screenshot-mobile.png)

### Links

- Solution URL: [GitHub Repository](https://github.com/noob-coder6/Product-preview-page.git)
- Live Site URL: [Live Demo](https://your-live-site-url.com)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties (CSS variables)
- Flexbox
- CSS Grid
- Mobile-first workflow
- Responsive images with `<picture>` element
- BEM naming convention

### What I learned

This project helped me solidify several key concepts:

**1. Responsive Images with the `<picture>` element**

I learned how to implement art direction using the `<picture>` element to serve different images based on screen size:
```html
<picture class="product-card__image">
  <source media="(min-width: 600px)" srcset="./images/image-product-desktop.jpg">
  <img src="./images/image-product-mobile.jpg" alt="Gabrielle Essence Eau De Parfum bottle">
</picture>
```

**2. CSS Custom Properties for maintainable code**

Using CSS variables made it easy to maintain consistent colors and typography throughout the project:
```css
:root {
  --clr-primary-green-500: hsl(158, 36%, 37%);
  --clr-primary-green-700: hsl(158, 42%, 18%);
  --ff-montserrat: 'Montserrat', sans-serif;
  --ff-fraunces: 'Fraunces', serif;
}
```

**3. Flexbox layout switching**

I learned how to efficiently switch layouts from mobile (column) to desktop (row) using flexbox:
```css
.product-card {
  display: flex;
  flex-direction: column; /* Mobile: stacked */
}

@media (min-width: 600px) {
  .product-card {
    flex-direction: row; /* Desktop: side-by-side */
  }
}
```

**4. Modern CSS centering with Grid**

Using CSS Grid's `place-items` property to center content both horizontally and vertically:
```css
body {
  display: grid;
  place-items: center;
  min-height: 100vh;
}
```

**5. Accessible button states**

Implementing proper hover and focus states for better user experience and accessibility:
```css
.product-card__add-to-cart:hover,
.product-card__add-to-cart:focus {
  background-color: var(--clr-primary-green-700);
  outline: none;
}
```

### Continued development

Areas I want to focus on in future projects:

- **Advanced CSS animations**: Adding micro-interactions and subtle animations to enhance user experience
- **CSS Grid layouts**: Exploring more complex grid-based layouts for larger projects
- **Accessibility improvements**: Better keyboard navigation and screen reader support
- **Performance optimization**: Image optimization techniques and lazy loading
- **CSS preprocessors**: Learning SASS/SCSS for more powerful styling capabilities

## Author

- Frontend Mentor - [@noob-coder6](https://www.frontendmentor.io/profile/noob-coder6)