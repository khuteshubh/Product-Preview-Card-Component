# Product-Preview-Card-Component


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
This is Product Card Component.

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover and focus states for interactive elements

### Screenshot

![](./Screenshot%202022-12-16%20at%2001-52-35%20Product%20preview%20card%20component.png)



### Links

- Solution URL: (https://github.com/khuteshubh/Product-Preview-Card-Component.git)
- Live Site URL: [(https://khuteshubh.github.io/Product-Preview-Card-Component/)]

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox

### What I learned

Use this section to recap over some of your major learnings while working through this project. Writing these out and providing code samples of areas you want to highlight is a great way to reinforce your own knowledge.

To see how you can add code snippets, see below:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0"> <!-- displays site properly based on user's device -->
  <meta name="author"   content="Shubham khute">
  <meta name="keyword"  content="html,css">
  <link rel="icon" type="image/png" sizes="32x32" href="./images/favicon-32x32.png">

  <link rel="stylesheet" href="./style.css">
  <title>Product preview card component</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.2.1/css/all.min.css">
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,700&family=Montserrat:wght@500;700&display=swap" rel="stylesheet">
</head>
<body>

  <main>
    <div class="whole-card">
      <div><img class="perfume-bottle" src="./image-product-mobile.jpg" alt="chanel-perfume" aria-label="perfume"> 
        <img class="desktop-perfume-bottle" src="./image-product-desktop.jpg" alt="desktop-size-perfume"></div>

        <div class="card-text">
          <p class="perfume">PERFUME</p>
          <h1>Gabrielle Essence Eau De Parfum</h1>
          <p class="card-info">
            A floral, solar and voluptuous interpretation composed by Olivier Polge,
            Perfumer-Creator for the House of CHANEL.
          </p>
          <span class="prices">
            <span class="sale-price">$149.99</span>
            <span class="regular-price">$169.99</span>
          </span>
          <button>  Add to Cart</button>
        </div>
      

    </div>
  </main>
  
  
</body>
</html>

```
```css
:root {
    --dark-cyan: hsl(158, 36%, 37%);
    --cream: hsl(30, 38%, 92%);
    --very-dark-blue: hsl(212, 21%, 14%);
    --dark-grayish-blue: hsl(228, 12%, 48%);
    --white: hsl(0, 0%, 100%);
    --fraunces: 'Fraunces', serif;
    --montserrat: 'Montserrat', sans-serif;
}

body {
	background-color: var(--cream);
    font-size: 14px;
    font-family: var(--montserrat);
    align-items: center;
    display: flex;
    flex-direction: column;
    justify-content: center;
    margin: 0;
    min-height: 100vh;
}

h1 {
    font-size: 32px;
    line-height: 2rem;
    color: var(--very-dark-blue);
}

h1, #sale-price {
    font-family: var(--fraunces);
}

p, h1 {
    padding: 0px 20px 0px 20px;
}

button {
    color: white;
    font-size: 14px;
    font-weight: 700;
    font-family: var(--montserrat);
    padding: 13px 100px;
    margin: 0px 0px 20px 20px;
    background-color: var(--dark-cyan);
    border: 1px solid var(--dark-cyan);
    border-radius: 7px;
    margin-bottom: 25px;
}

button:hover {
    background-color: hsl(158, 37%, 13%);
    border: 1px solid hsl(158, 37%, 13%);
}

.card-text {
    width: 350px;
    background-color: var(--white);
    border-radius: 0px 0px 10px 10px;
}

.perfume, .regular-price, .card-info {
    color: var(--dark-grayish-blue);
}

.perfume-bottle {
    width: 350px;
    border-radius: 10px 10px 0px 0px;
    position: relative;
    top: 18px;
}

.desktop-perfume-bottle {
    display: none;
}

.perfume {
    letter-spacing: .3rem;
    margin-bottom: 0px;
    padding-top: 15px;
    position: relative;
    top: 10px;
    font-size: 12px;
}

.card-info {
    line-height: 1.5rem;
}

.prices {
    display: flex;
    flex-direction: row;
}

.sale-price {
    color: var(--dark-cyan);
    font-size: 32px;
    padding: 20px 20px 0px 20px;
    margin: 15px 0px 15px 0px;
}

.regular-price {
    align-self:center;
    text-decoration: line-through;
    position: relative;
    top: 7px;
}

.cart-icon {
    position: relative;
    top: 3px;
    padding-right: 5px;
}



/*desktop styling*/

@media (min-width: 900px) {
    img {
        border-radius: 10px 0px 0px 10px;
    }
    
    button {
        display: block;
        margin: 0 auto;
        padding: 14px 74px;
    }
    
    .whole-card {
        display: flex;
    }

    .card-text {
        width: 285px;
        padding: 10px 10px 10px 10px;
        border-radius: 0px 10px 10px 0px;
    }

    .sale-price {
        padding-top: 0px;
        padding-bottom: 10px;
    }

    .regular-price {
        padding-bottom: 20px;
    }

    .card-info {
        padding-right: 35px;
    }

    .perfume {
        padding-top: 0px;
    }

    .perfume-bottle {
        display:none;
    }

    .desktop-perfume-bottle {
        display: block;
        width: 300px;
    }
}
 ...


If you want more help with writing markdown, we'd recommend checking out [The Markdown Guide](https://www.markdownguide.org/) to learn more.

**Note: Delete this note and the content within this section and replace with your own learnings.**

### Continued development

Use this section to outline areas that you want to continue focusing on in future projects. These could be concepts you're still not completely comfortable with or techniques you found useful that you want to refine and perfect.

**Note: Delete this note and the content within this section and replace with your own plans for continued development.**

### Useful resources

- [Example resource 1](https://www.w3schools.com/cssref/css3_pr_flex.php) - This helped me for design flexible responsive layout structure without using float or positioning. I really liked this pattern and will use it going forward.
- [Example resource 2](https://www.w3schools.com/css/css_positioning.asp) - This is an amazing website which helped me finally understand positioning method. I'd recommend it to anyone still learning this concept.



## Author

- Linkedin - [shubham suresh khute](https://www.linkedin.com/in/shubham-khute-0611211a6/)
- Frontend Mentor - [@khuteshubh](https://www.frontendmentor.io/profile/khuteshubh)





