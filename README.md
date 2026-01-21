# Frontend Mentor - Product preview card component solution

This is a solution to the [Product preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/product-preview-card-component-GO7UmttRfa). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

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

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover and focus states for interactive elements

### Links

- Solution URL: [FM Product preview component](https://github.com/galvaradosd/FM-Product-preview-component)
- Live Site URL: [live site URL](https://your-live-site-url.com)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties (CSS Variables)
- CSS Logical Properties
- Flexbox
- CSS Grid
- Mobile-first workflow
- BEM methodology
- Google Fonts (Montserrat & Fraunces)
- Responsive images with `<picture>` element

### What I learned

This project helped me solidify several modern CSS and HTML concepts:

#### 1. CSS Logical Properties for Internationalization

I used CSS logical properties instead of physical properties to make the component future-proof for different writing modes and languages:

```css
.product-card {
	inline-size: 100%;
	block-size: auto;
	padding-block: var(--space-lg);
	padding-inline: var(--space-xl);
	margin-block-end: 1rem;
}
```

#### 2. BEM Methodology for Scalable CSS

Implemented BEM naming convention for better code organization and maintainability:

```html
<article class="product-card">
	<div class="product-card__content">
		<h1 class="product-card__title">...</h1>
		<p class="product-card__price product-card__price--current">...</p>
	</div>
</article>
```

#### 3. Responsive Images with Picture Element

Used the `<picture>` element for art direction and better performance:

```html
<picture class="product-card__picture">
	<source
		media="(min-width: 640px)"
		srcset="assets/images/image-product-desktop.jpg"
	/>
	<img
		src="assets/images/image-product-mobile.jpg"
		alt="Gabrielle Essence Eau De Parfum perfume bottle"
		class="product-card__image"
	/>
</picture>
```

#### 4. CSS Grid with Full Height Image

Learned how to make images occupy full container height in a CSS Grid layout:

```css
.product-card {
	display: grid;
	grid-template-columns: 1fr 1fr;
	grid-template-rows: 1fr;
}

.product-card__figure,
.product-card__picture {
	block-size: 100%;
	display: flex;
}

.product-card__image {
	block-size: 100%;
	object-fit: cover;
	object-position: center;
}
```

#### 5. CSS Custom Properties for Design System

Created a comprehensive design token system:

```css
:root {
	--color-primary-green-500: hsl(158, 36%, 37%);
	--color-primary-green-700: hsl(158, 42%, 18%);
	--font-family-primary: "Montserrat", sans-serif;
	--font-family-accent: "Fraunces", serif;
	--space-lg: 1.5rem;
	--border-radius-card: 0.625rem;
	--transition-default: 0.3s ease;
}
```

#### 6. Accessibility Best Practices

Implemented semantic HTML and ARIA attributes for better accessibility:

```html
<span class="visually-hidden">Current price:</span>
<img src="icon.svg" alt="" aria-hidden="true" />
```

### Continued development

Areas I want to continue focusing on in future projects:

- **CSS Container Queries**: Explore container queries for even more flexible responsive designs
- **CSS Animations**: Add subtle animations and micro-interactions
- **Performance Optimization**: Implement lazy loading and image optimization techniques
- **CSS Modules**: Explore CSS-in-JS solutions for component-based architecture
- **Advanced Grid Layouts**: Master more complex CSS Grid patterns

### Useful resources

- [CSS Logical Properties - MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Logical_Properties) - Helped me understand and implement logical properties for better internationalization
- [BEM Methodology](https://getbem.com/) - Great resource for understanding BEM naming conventions
- [CSS Grid Guide - CSS Tricks](https://css-tricks.com/snippets/css/complete-guide-grid/) - Comprehensive guide that helped with the grid layout
- [Modern CSS Reset](https://piccalil.li/blog/a-modern-css-reset/) - Used as inspiration for the CSS reset
- [The Picture Element - Web.dev](https://web.dev/learn/design/picture-element/) - Excellent guide on responsive images

## Author

- Frontend Mentor - [@galvaradosd](https://www.frontendmentor.io/profile/galvaradosd)
- GitHub - [@galvaradosd](https://github.com/galvaradosd)
