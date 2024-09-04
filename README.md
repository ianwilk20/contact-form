# Frontend Mentor - Contact form solution

This is a solution to the [Contact form challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/contact-form--G-hYlqKJj). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

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

- Complete the form and see a success toast message upon successful submission
- Receive form validation messages if:
  - A required field has been missed
  - The email address is not formatted correctly
- Complete the form only using their keyboard
- Have inputs, error messages, and the success message announced on their screen reader
- View the optimal layout for the interface depending on their device's screen size
- See hover and focus states for all interactive elements on the page

### Screenshot

Desktop:

![Desktop initial state](/design/sol-desktop-init.png)

![Desktop filled state](/design/sol-desktop-filled.png)

![Desktop submitted state](/design/sol-desktop-submitted.png)

Mobile: 

![Mobile initial state](/design/sol-mobile-init.png)


### Links

- [Solution URL](https://github.com/ianwilk20/contact-form)
- [Live Site URL](https://contact-form-ianwilk20.netlify.app/design/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Mobile-first workflow

### What I learned

I learned that even if you put two input's of type radio button in a fieldset it doesn't automatically group them, which means you'll be able to select more than one. To restrict users having one radio button selection at a time you need to give each radio button the same name property, ex. ```name="query-type"```. Providing the same name for multiple radio buttons groups them and restricts users from having more than one radio button selected at once. 

I learned that if you have text input inside of a form and you mark that field as required a few cool things occur. The browser will handle validation for you, in this case, when the user tries to submit the form, the browser will complain and say that the field is required. To do away with browser validation and handle it yourself you can specify ```novalidate``` on the form element; however, this means that you must handle all validation yourself.


I learned that the css pseudo-class ```:has()``` can be used for selecting a child element from parent. In the code, I have an outer div that wraps the "General Inquiry" radio button and the same for the "Support Request" radio button. The purpose of the outer div is to hold the radio button and for styling reasons. When either radio button is clicked the same behaviour styling should be applied to their respective outer div's - they need to have a light green highlight, a green border, and a green radio button. I used ```:has()``` on the outer div and specifed the child radio button in the function parameter. Ex. ```#outer-div:has(> #general-inqury-radio:checked)```. In turn this will apply styling to the outer-div when either of these two radio buttons is selected.

I learned how to customize a checkbox using CSS. See Useful resources for more details.

### Continued development

I think the most difficult part of this challenge was making the form look like the attached mockups. The JavaScript for form validation and submission, and the HTML took the least amount of time. For that reason, I think I need to improve my CSS skills.


### Useful resources

- [Documentation on the :has() pseudo-class](https://www.w3.org/TR/selectors-4/#) and [Example of :has()](https://stackoverflow.com/questions/1014861/is-there-a-css-parent-selector) -  Both of these resources helped me understand how to use the :has() pseudo-class
- [How to style a checkbox using CSS](https://sentry.io/answers/how-to-style-a-checkbox-using-css/) - This article was a great resource for how to apply custom styling to a checkbox.

## Author

- GitHub - [ianwilk20](https://github.com/ianwilk20)