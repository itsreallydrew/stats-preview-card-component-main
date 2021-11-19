# Frontend Mentor - Stats preview card component solution

This is a solution to the [Stats preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/stats-preview-card-component-8JqbgoU62). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

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

This is my second challenge from frontend mentor where I am building a stats card.

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size

### Screenshot

![Screenshot 2021-11-19 at 15-40-41 Frontend Mentor Stats preview card component](https://user-images.githubusercontent.com/88289750/142695232-7ce7798d-add6-47e2-ad2c-151798d99103.png)

### Links

- Solution URL: [Solution](https://www.frontendmentor.io/solutions/responsive-stats-card-component-using-css-grid-87yzEwRjG)
- Live Site URL: [Live Site](https://unruffled-darwin-9194d3.netlify.app)

## My process

I once again wanted to approach this problem using CSS grid. I feel like I have more control in placing items where I want when I use grid. I decided to go with a desktop first approach and figure out how to center the card itself in the middle of the page. At first I used only two rows and no columns, but then I realized that didn't translate well for mobile. I then decided to use 3 columns and have the center column take up a percentage of the viewport width. From there I have begun to understand that using vw and vh units makes it much easier to create a responsive layout.

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Sass/SCSS

### What I learned

The biggest thing I learned was how to set the opacity to create the overlay effect. This took me a lot longer than I believed it would to figure out. But I am glad I was able to discover. I set up the basic desktop layout relatively easily but this was my biggest hurdle.

The next most difficult thing was making the layout for mobile. At first I was struggling because everything was out of wack. But I learned that by resizing the rows and columns it was much easier to adjust the display than I initially believed.

Below is my code for the layout in desktop size and the specified mobile view:

```css
.container {
	background-color: $primary-1;
	display: grid;
	grid-template-rows: 90vh 1fr;
	grid-template-columns: 1fr 80vw 1fr;
	justify-items: center;
	align-items: center;

	@media only screen and (max-width: $mobile) {
		grid-template-columns: 1fr;
		grid-template-rows: min-content 1fr;
		padding: 2rem;
	}
}
```

### Continued development

Grid. That's the most I can say. I still need more practice but I'm glad that I'm pushing myself but deciding to use it in every project.

### Useful resources

- [Border radius on image](https://stackoverflow.com/questions/52151652/border-radius-if-there-is-an-image-on-the-border) - This helped me solve the issue where I was having trouble adding a border radius to the image automatically instead of manually applying it to match up with its parent container. Extremely helpful!

## Author

- Frontend Mentor - [@itsreallydrew](https://www.frontendmentor.io/profile/itsreallydrew)

## Acknowledgments

This is where you can give a hat tip to anyone who helped you out on this project. Perhaps you worked in a team or got some inspiration from someone else's solution. This is the perfect place to give them some credit.

**Note: Delete this note and edit this section's content as necessary. If you completed this challenge by yourself, feel free to delete this section entirely.**
