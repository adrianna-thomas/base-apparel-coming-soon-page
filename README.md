# Frontend Mentor - Base Apparel coming soon page solution

This is a solution to the [Base Apparel coming soon page challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/base-apparel-coming-soon-page-5d46b47f8db8a7063f9331a0). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Useful resources](#useful-resources)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the site depending on their device's screen size
- See hover states for all interactive elements on the page
- Receive an error message when the `form` is submitted if:
  - The `input` field is empty
  - The email address is not formatted correctly

### Screenshot

![](./screenshots/mobile-screenshot.png)
![](./screenshots/mobile-screenshot-active.png)
![](./screenshots/desktop-screenshot.png)
![](./screenshots/desktop-screenshot-active.png)

### Links

- Solution URL: [Frontend Mentor Solution Page](https://www.frontendmentor.io/solutions/base-apparel-coming-soon-page-ryBiaUlB5)
- Live Site URL: [GitHub Deployed Page](https://adrianna-thomas.github.io/base-apparel-coming-soon-page/)
- Github Repository: [GitHub](https://github.com/adrianna-thomas/base-apparel-coming-soon-page)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox

### What I learned

Learned how to add animation to html elements.


```css
h1,
p {
  transform: translateX(-100%);
  animation: comeinleft 0.5s ease forwards;
}

@keyframes comeinleft {
  to {
    transform: translateX(0);
  }
}
```

I learned how to style the placeholder text inside a form.

```html
input::placeholder { color: var(--Desaturated-Red); font-weight: 200; font-size: 14px; }
```


```

Used HTML form validation with Javascript to display error message when input is not valid.

```js
form.addEventListener("submit", (e) => {
  e.preventDefault();
  const emailVal = email.value;

  //check if it is a valid email
  if (!validateEmail(emailVal)) {
    form.classList.add("error");
  } else {
    form.classList.remove("error");
    document.body.innerHTML = "Thank you!";
  }
});
```


### Useful resources

- [CSS Placeholder formatting](https://www.w3schools.com/howto/howto_css_placeholder.asp) - Helped me change the text color of the form placeholder.

- [Button inside input field](https://www.geeksforgeeks.org/how-to-put-a-responsive-clear-button-inside-html-input-text-field/) - This helped me understand how to position the arrow button inside the input field.

## Author

- Frontend Mentor - [@adrianna-thomas](https://www.frontendmentor.io/profile/adrianna-thomas)

## Acknowledgments

1. [Florin Pop's Youtube](https://www.youtube.com/watch?v=8A7-0gsbHA0&ab_channel=FlorinPop) - This helped me figure out how to approach the Javascript by adding an error class and creating related styles.
