# Frontend Mentor - Social links profile solution

This is a solution to the [Social links profile challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/social-links-profile-UG32l9m6dQ). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

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

- See hover and focus states for all interactive elements on the page

### Screenshot

![](./screenshot.jpg)

Add a screenshot of your solution. The easiest way to do this is to use Firefox to view your project, right-click the page and select "Take a Screenshot". You can choose either a full-height screenshot or a cropped one based on how long the page is. If it's very long, it might be best to crop it.

Alternatively, you can use a tool like [FireShot](https://getfireshot.com/) to take the screenshot. FireShot has a free option, so you don't need to purchase it.

Then crop/optimize/edit your image however you like, add it to your project, and update the file path in the image above.

**Note: Delete this note and the paragraphs above when you add your screenshot. If you prefer not to add a screenshot, feel free to remove this entire section.**

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow
- [React](https://reactjs.org/) - JS library
- [Next.js](https://nextjs.org/) - React framework
- [Styled Components](https://styled-components.com/) - For styles

**Note: These are just examples. Delete this note and replace the list above with your own choices**

### What I learned

#### html- accessibility

###### Using `aria-label` for External Links

```html
<a
  href="https://github.com"
  class="button"
  target="_blank"
  rel="noopener noreferrer"
  aria-label="GitHub (opens in a new tab)"
  >GitHub</a
>
<a
  href="https://www.frontendmentor.io"
  class="button"
  target="_blank"
  rel="noopener noreferrer"
  aria-label="Frontend Mentor (opens in a new tab)"
  >Frontend Mentor</a
>
```

###### Background of the Use Case:

- Social Media Profile Links: A webpage displays links to various social media profiles (GitHub, LinkedIn, Twitter, etc.).
- Links Open in a New Tab: Each link opens in a new browser tab when clicked, which is a behavior that users should be informed about for better accessibility.
- Clean UI Design: The design aims to be clean and uncluttered, avoiding redundant visible text that could overwhelm sighted users.
  
###### Why We Need to Use aria-label:
- Informing Screen Reader Users: aria-label provides essential information to screen reader users, letting them know both the purpose of the link and that it opens in a new tab.
- Accessibility Enhancement: Ensures that users with visual impairments understand the behavior of the links without needing to see visible text.
- Avoiding Visible Clutter: Keeps the UI clean by avoiding extra text like "(opens in a new tab)" in the visible link labels, while still conveying this information through aria-label.
- Consistency Across Links: Provides a uniform experience across all links, making the webpage easier to navigate for users relying on assistive technologies.
- Better than title Attribute: More reliably supported by screen readers compared to the title attribute, ensuring the information is conveyed effectively.

#### html- secuirty
##### `rel="noopener noreferrer"` prevent "reverse tabnabbing" attack when using target=“_blank”
```html
<a
  href="https://github.com"
  class="button"
  target="_blank"
  rel="noopener noreferrer"
  aria-label="GitHub (opens in a new tab)"
  >GitHub</a
>
```
- Security and Performance: When using target="_blank" to open links in a new tab, the newly opened tab retains a connection back to the original page via the window.opener object. This can pose a security risk because the new tab can potentially manipulate the original page's content or redirect it to a malicious site.
- rel="noopener": Adding rel="noopener" prevents the new tab from gaining access to the window.opener object, effectively cutting the connection between the original page and the new tab. This improves security by protecting the original page from potential malicious actions.
- rel="noreferrer": Adding rel="noreferrer" alongside noopener also ensures that no referral information (i.e., the URL of the original page) is sent to the new tab, further enhancing privacy.
- The Problem: This vulnerability, known as the "reverse tabnabbing" attack, can be exploited by attackers to trick users or hijack the original page. Using rel="noopener noreferrer" mitigates this risk, ensuring safer browsing for users.

### Continued development

Use this section to outline areas that you want to continue focusing on in future projects. These could be concepts you're still not completely comfortable with or techniques you found useful that you want to refine and perfect.

**Note: Delete this note and the content within this section and replace with your own plans for continued development.**

### Useful resources

- [Example resource 1](https://www.example.com) - This helped me for XYZ reason. I really liked this pattern and will use it going forward.
- [Example resource 2](https://www.example.com) - This is an amazing article which helped me finally understand XYZ. I'd recommend it to anyone still learning this concept.

**Note: Delete this note and replace the list above with resources that helped you during the challenge. These could come in handy for anyone viewing your solution or for yourself when you look back on this project in the future.**

## Author

- Website - [Add your name here](https://www.your-site.com)
- Frontend Mentor - [@yourusername](https://www.frontendmentor.io/profile/yourusername)
- Twitter - [@yourusername](https://www.twitter.com/yourusername)

**Note: Delete this note and add/remove/edit lines above based on what links you'd like to share.**

## Acknowledgments

This is where you can give a hat tip to anyone who helped you out on this project. Perhaps you worked in a team or got some inspiration from someone else's solution. This is the perfect place to give them some credit.

**Note: Delete this note and edit this section's content as necessary. If you completed this challenge by yourself, feel free to delete this section entirely.**
