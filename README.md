# Frontend Mentor - Advice generator app solution

This is a solution to the [Advice generator app challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/advice-generator-app-QdUG-13db). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the app depending on their device's screen size
- See hover states for all interactive elements on the page
- Generate a new piece of advice by clicking the dice icon

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

### Built with

- HTML5 markup
- CSS custom properties
- Flexbox
- Vue.js [JavaScript Framework]
- Vite.js

### What I learned

Use this section to recap over some of your major learnings while working through this project. Writing these out and providing code samples of areas you want to highlight is a great way to reinforce your own knowledge.

To see how you can add code snippets, see below:

```Get data from API
fetchAdvice() {
      axios
        .get("https://api.adviceslip.com/advice")
        .then((response) => {
          this.advice = response.data.slip.advice;
          this.id = response.data.slip.id;
        })
        .catch((error) => {
          console.error(error);
        });
    },
```

## Author

- Website - [Eurico Santos](https://portfolio-react-bizhead.vercel.app/)
- Frontend Mentor - [@Bizhead](https://www.frontendmentor.io/profile/Bizhead)
- Linkedin - [@eurico-santos](https://www.linkedin.com/in/eurico-santos-545b57109)
