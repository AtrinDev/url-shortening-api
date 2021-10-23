# Shortly URL shortening API Challenge solution

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the site depending on their device's screen size
- Shorten any valid URL
- See a list of their shortened links, even after refreshing the browser
- Copy the shortened link to their clipboard in a single click
- Receive an error message when the `form` is submitted if:
  - The `input` field is empty

### Screenshot

![](design/desktop-design.jpg)

### Links

- GitHub URL: [GitHub Repository](https://your-solution-url.com)
- Live Site URL: [GitHub Pages](https://your-live-site-url.com)

## My process

### Built with

- Semantic HTML5 markup
- CSS3 custom properties
- javaScript (ES6)
- Bootstrap 4
- Flexbox
- CSS Grid

### What I learned

This project, despite being simple and small, taught me good and small points. Tips that will help me a lot in the future. It was a good experience overall.

To see how you can add code snippets, see below:

```html
<div class="row mx-auto stats">
  <div class="col-xs-12 mx-auto featured-box box-1">
    <div class="d-inline-block stats-icon">
      <img src="images/icon-brand-recognition.svg" alt="brand" />
    </div>
    <h3 class="stats-title">Brand Recognition</h3>
    <p class="stats-info">
      Boost your brand recognition with each click. Generic links don’t mean a
      thing. Branded links help instil confidence in your content.
    </p>
  </div>
  <div class="col-xs-12 mx-auto featured-box box-2">
    <div class="d-inline-block stats-icon">
      <img src="images/icon-detailed-records.svg" alt="records" />
    </div>
    <h3 class="stats-title">Detailed Records</h3>
    <p class="stats-info">
      Gain insights into who is clicking your links. Knowing when and where
      people engage with your content helps inform better decisions.
    </p>
  </div>
  <div class="col-xs-12 mx-auto featured-box box-3">
    <div class="d-inline-block stats-icon">
      <img src="images/icon-fully-customizable.svg" alt="customizable" />
    </div>
    <h3 class="stats-title">Fully Customizable</h3>
    <p class="stats-info">
      Improve brand awareness and content discoverability through customizable
      links, supercharging audience engagement.
    </p>
  </div>
</div>
```

```css
@media screen and (min-width: 992px) {
  .stats {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    grid-gap: 2rem;
  }
  .stats::before {
    content: "";
    position: absolute;
    top: 50%;
    left: 25%;
    width: 50%;
    height: 0.5rem;
    background-color: #2bd0d0;
  }
  .box-1 {
    margin-bottom: 6rem;
  }
  .box-2 {
    margin-top: 3rem;
    margin-bottom: 3rem;
  }
  .box-3 {
    margin-top: 6rem;
  }
}
```

```js
function shortUrl() {
  const input = document.getElementById("input").value;
  document.getElementById("userLink").innerHTML = input;
  fetch(`https://api.shrtco.de/v2/shorten?url=${input}/`)
    .then((response) => response.json())
    .then((res) => {
      document.getElementById("shrtLnk").value = res.result.short_link;
    });
}
```

## Author

- Website - [My Website](https://www.atrindev.ir)
- Linkedin - [My Linkedin](https://www.linkedin.com/in/atrindev)
