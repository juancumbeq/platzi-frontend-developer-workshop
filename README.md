# Frontend Developer Practical Course

<p align="center">
  <img src="https://img.shields.io/badge/Curso%20-Finalizado-brightgreen"/>
</p>

<br>

Aclaración sobre los siguientes pasos
Este es el primero de cuatro cursos, en los que Platzi te llevará de la mano para que puedas tener construir una aplicación web o tienda virtual.

Maquetado → estás aquí
React
API REST con Express.js
Base de Datos con PostgreSQL

<br>

## What did I Learn Through this Course:
  - Introducction to frontend development
  - HTML layout
  - CSS layout
  - Responsive Design
  - CSS architecture

<br>
<br>

## Index
  - [INTRODUCCTION TO FRONTEND DEVELOPMENT](#introduction-to-frontend-development)
    - [What are HTML and CSS? What are they used for?](#what-is-html-and-css-what-are-they-used-for)
      - [What is HTML?](#what-is-html)
      - [What is CSS?](#what-is-css)
    - [Render Engines: From Files to Pixels](#render-engines-from-files-to-pixels)
      - [Which is the browser engine?](#which-is-the-browser-engine)
      - [Rendering Process](#rendering-process)

<br>
<br>
<br>

# INTRODUCTION
  ## CSS Good Practices: Reflection and Warning
# LAYOUT AND COMPONENTS
  ## Identify your Project Screens
  ## Design System, Assets and CSS Variables
# RESPONSIVE LAYOUT: AUTHENTICATION SCREENS
  ## Create New Password: HTML
  ## Create New Password: CSS
  ## Mail sent
  ## Login
  ## Create and Edit my Account
  ## My Account
# RESPONSIVE LAYOUT: MAIN VIEWS
  ## Home Page: HTML
  ## Home Page: CS
  ## Desktop Menu
  ## Mobile Menu
  ## My Purchase Order: HTML
  ## My Purchase Order: CSS
  ## My Orders
  ## Navbar: HTML
  ## Navbar: CSS
  ## Product Details
  ## Shopping Cart: HTML
# NEXT STEPS

<br>
<br>
<br>

# INTRODUCTION
  ## [CSS Good Practices: Reflection and Warning]()

  ### What is a good practice?

Good practices are a set of customs, actions, decisions, and/or tools that streamline, improve performance, readability, maintenance, and/or scalability of our projects in a very specific CONTEXT.

The keyword is context. Good practices are NOT absolute. Just as they work in certain situations, they may not make sense in other circumstances.

It is a common mistake to talk about good or bad practices without understanding their context correctly.

<br>

  ### The context of this course

The Practical Frontend Developer Course belongs to two schools in Platzi:

  * The JavaScript professional route: it is the shortest route to learn web development from scratch to a very advanced level with the PERNN Stack (PostgreSQL, Express.js, React.js, Next.js, and Node.js).

  * Web Development School: the longest and most complete learning path to master and delve into all the most important programming tools or stacks of web development.
💡 JavaScript School vs. Web Development School: Which one to choose? Which one is better?

Along with the Frontend Developer Course, this course is the introduction to the great world of HTML and CSS layout that we will study in the JavaScript School. After this course, we will continue with the basics of JavaScript, frontend with React.js, and backend with Node.js.

In contrast, in the Web Development School, we have many more courses to practice HTML and CSS, create even more projects for your professional portfolio, and delve into complex tools such as responsive design, CSS Grid, flexbox, and CSS animations.

<br>

  ### Style tag vs. .css files

In the next classes, you may wonder why we decided not to separate the styles into their own .css files if it is supposedly a "bad practice." But remember that good or bad practices are NOT absolute, they always depend on a context.

Later on your learning path, you will take the Practical React.js Course. One of its objectives is to teach you how to convert pages in HTML and CSS to components in React. You will realize that there we download the project from this Frontend Developer Practical Course to separate it into views, components, and containers.

The reason for keeping the HTML and CSS of each section of our store in a single .html file is to facilitate our work of separating and joining all that code when we take the React course.

<br>

  ### Conclusions

If your project with HTML and CSS is the final version of the application that you will deploy to production (the one you will publish on the internet and will be used by real users), then it is definitely a very good practice to separate your styles into .css files.

On the other hand, if your layout with HTML and CSS is just the beginning of your frontend development and later you will convert these elements into components with a tool like Web Components, React.js, Angular, Svelte, or Vue.js, then it is NOT a bad practice to separate each element into its respective file or keep its HTML and CSS in the same place.

I hope this explanation has helped you understand a little about the development flow and decisions we made in this course. Always remember to have a very clear understanding of the context of each situation before determining if it is a good or bad practice.

<br>
<br>
<br>

# LAYOUT AND COMPONENTS
  ## [Identify your Project Screens](https://scene.zeplin.io/project/60afeeed20af1378ed046538)
Web layout or web design consists of transforming a graphic design —a sketch— (made by UX/UI in Figma or Sketch) into a functional interface in terms of programming that a specific browser or device understands.

<p align="center">
  <img src="https://github.com/juancumbeq/platzi-frontend-developer-workshop/blob/main/readme_images/shopping-cart.png?raw=true" width= "35%" alt="Shopping Cart">
</p>

The design area provided us with the project sketch in [Figma](https://scene.zeplin.io/project/60afeeed20af1378ed046538).
We can identify the views of:

  * Home
  * Account creation
  * Access
  * Shopping cart
  * Purchase order
  * Product detail
  * Menu

<p align="center">
  <img src="https://github.com/juancumbeq/platzi-frontend-developer-workshop/blob/main/readme_images/project.png?raw=true" width= "99%" alt="Project">
</p>

From here, you can see how the interaction between the different screens works.

  * [Desktop version](https://www.figma.com/proto/bcEVujIzJj5PNIWwF9pP2w/Platzi_YardSale?node-id=0-999&amp%3Bscaling=scale-down&amp%3Bpage-id=0%3A998&amp%3Bstarting-point-node-id=5%3A2808)

  * [Mobile version](https://www.figma.com/proto/bcEVujIzJj5PNIWwF9pP2w/Platzi_YardSale?node-id=0%3A462&amp!%5Bshopping-cart.jpg%5D(https://static.platzi.com/media/user_upload/shopping-cart-4d77fd41-9393-4883-b66b-2ee40682f1ea.jpg)//platzi.com/categorias/diseno/)


  <br>
  <br>

  ## [Design System, Assets and CSS Variables]()
We're starting to work! We'll follow a design system that will allow us to achieve a uniform project. For this, **we'll declare variables in CSS** with the colors we'll use and organize icons and logos into folders.

[Shopify Blog](https://polaris.shopify.com/design/colors)

<br>

  ### What's the purpose of a design system?
The main advantage of implementing a design system is that it simplifies the tasks of designers and developers in the creation process. It also speeds up decision-making among teams.

<br>

  ### CSS Variables
In CSS, we call variables to custom properties.
They contain specific values that can be reused many times in a document.

They're established using double dashes notation
```
--variable-name: value;
```

They're accessed using the ``var()`` function
```
property: var(--variable-name);
```
Normally, we declare them inside the ``:root`` selector so their scope is global.

Our project would look like this:
```
:root {
    --black:#000000;
    --white: #FFFFFF;
    --very-light-pink: #C7C7C7;
    --text-input-field: #F7F7F7;
    --dark: #232830;
    --hospital-green: #ACD9B2;
}
```
The scope of CSS variables declared using another pseudo-class will be limited to the selector within which they are declared. Unlike variables declared within the :root pseudo-class, which have global scope and can be accessed anywhere in the document, variables declared within other selectors have a more limited scope.

For example, if you declare variables within a specific selector like .container, those variables will only be accessible within elements that are descendants of the .container class. They won't be available globally throughout the document.

Here's an example:
```
.container {
    --primary-color: blue;
}

.element {
    color: var(--primary-color); /* This will work */
}

.another-element {
    color: var(--primary-color); /* This won't work */
}
```
In this example, the --primary-color variable is declared within the .container selector. Therefore, it can be used within any element that is a descendant of .container, such as .element. However, it cannot be used outside of that scope, as demonstrated by .another-element.


You can also name your variables according to their function.
Examples: ``--background-color``, ``--primary-color``, etc.

<br>

  ### Fonts
We'll look for the fonts proposed by the design in [Google Fonts](https://fonts.google.com/specimen/Quicksand)
We place the links inside the HTML head tag
```
<head>
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Quicksand:wght@300;500;700&display=swap" rel="stylesheet">
</head>
```

Inside the style tag, we tell CSS to implement it
```
body {
    font-family: 'Quicksand', sans-serif;
}
```

<br>
<br>
<br>

# RESPONSIVE LAYOUT: AUTHENTICATION SCREENS
  ## [Create New Password: HTML](https://github.com/juancumbeq/platzi-frontend-developer-workshop/blob/main/project/1-create-new-password.html)
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Quicksand:wght@300;500;700&display=swap" rel="stylesheet">

  <title>Yard Sale</title>

</head>
<body>
  <div class="login">
    <div class="form-container">
      <img src="../resources/logos/logo_yard_sale.svg" alt="logo" class="logo">

      <h1 class="title">Create a new password</h1>
      <p class="subtitle">Enter a new password for your account</p>

      <form action="/" class="form">

        <label for="password" class="label">Password</label>
        <input type="password" class="input input-password" id='password' placeholder='*********'>

        <label for="password" class="label">Password</label>
        <input type="password" class="input input-password" id='new-password' placeholder='*********'>
        
        <input type="submit" value="Confirm" class='primary-button login-button'>
      </form>
    </div>
  </div>
</body>
</html>
```

<br>
<br>

  ## [Create New Password: CSS](https://github.com/juancumbeq/platzi-frontend-developer-workshop/blob/main/project/1-create-new-password.html)
Now we'll style the HTML for the **"new password"** screen. Design has suggested the following visual for both mobile and desktop. The only exception is that the logo should not be displayed in this latest version.

<p align="center">
  <img src="https://github.com/juancumbeq/platzi-frontend-developer-workshop/blob/main/readme_images/new-password.png?raw=true" width= "35%" alt="New password">
</p>

Which styles will we implement?
```
.login {
  width: 100%;
  height: 100vh;
  display: grid;
  place-items: center;
}
.form-container {
  display: grid;
  grid-template-rows: auto 1fr auto;
  width: 300px;
}
.logo {
  width: 150px;
  margin-bottom: 48px;
  justify-self: center;
  display: none;
}
.title {
  font-size: var(--lg);
  margin-bottom: 12px;
  text-align: center;
}
.subtitle {
  color: var(--very-light-pink);
  font-size: var(--md);
  font-weight: 300;
  margin-top: 0;
  margin-bottom: 32px;
  text-align: center;
}
.form {
  display: flex;
  flex-direction: column;
}
.label {
  font-size: var(--sm);
  font-weight: bold;
  margin-bottom: 4px;
}
.input {
  background-color: var(--text-input-field);
  border: none;
  border-radius: 8px;
  height: 30px;
  font-size: var(--md);
  padding: 6px;
  margin-bottom: 12px;
}
.primary-button {
  background-color: var(--hospital-green);
  border-radius: 8px;
  border: none;
  color: var(--white);
  width: 100%;
  cursor: pointer;
  font-size: var(--md);
  font-weight: bold;
  height: 50px;
}
.login-button {
  margin-top: 14px;
  margin-bottom: 30px;
}
@media (max-width: 640px) {
  .logo {
    display: block;
  }
}
```

<br>

  ### Using Grid Display to Center Elements
As you can see in our ``.login`` class, with just two lines of code, we can center our content:
```
display: grid;
place-items: center;
```

The ``place-items`` shorthand property allows you to align elements, both horizontally and vertically, in a container with Grid or Flexbox. That is, it is an abbreviation of the align-items and justify-items properties. If you don't specify the second value, it will use the first for both alignments.

Try different combinations and see what happens:

  * **place-items: center stretch;**
  * **place-items: center start;**
  * **place-items: start end;**
  * **place-items: end center;**

<br>

  ### How to Organize Styles
One way to do it is according to its purpose. Following the following order:

  * Positioning
  * Box model
  * Typography
  * Visuals
  * Others

See the detailed explanation [here](https://platzi.com/new-home/clases/2030-mobile-first/32304-estilos-base/).

<br>
<br>

  ## [Mail Sent](https://github.com/juancumbeq/platzi-frontend-developer-workshop/blob/main/project/2-mail-sent.html)
Now we will build the screen where the email has been sent by reusing the code. As a recommendation, start by creating the responsive version of the project.

<p align="center">
  <img src="https://github.com/juancumbeq/platzi-frontend-developer-workshop/blob/main/readme_images/mail-sent.png?raw=true" width= "35%" alt="Mail sent">
</p>

```
<div class="login">
  <div class="form-container">
    <img src="./logos/logo_yard_sale.svg" alt="logo" class="logo">

    <h1 class="title">Email has been sent!</h1>
    <p class="subtitle">Please check your inbox for instructions on how to reset the password</p>

    <div class="email-image">
      <img src="./icons/email.svg" alt="email">
    </div>

    <button class="primary-button login-button">Login</button>

    <p class="resend">
      <span>Didn't receive the email?</span>
      <a href="/">Resend</a>
    </p>
  </div>
</div>
```
<br>

  ### CSS Code
```
.login {
      width: 100%;
      height: 100vh;
      display: grid;
      place-items: center;
    }
    .form-container {
      display: grid;
      grid-template-rows: auto 1fr auto;
      width: 300px;
      justify-items: center;
    }
    .logo {
      width: 150px;
      margin-bottom: 48px;
      justify-self: center;
      display: none;
    }
    .title {
      font-size: var(--lg);
      margin-bottom: 12px;
      text-align: center;
    }
    .subtitle {
      color: var(--very-light-pink);
      font-size: var(--md);
      font-weight: 300;
      margin-top: 0;
      margin-bottom: 32px;
      text-align: center;
    }
    .email-image {
      width: 132px;
      height: 132px;
      border-radius: 50%;
      background-color: var(--text-input-field);
      display: flex;
      justify-content: center;
      align-items: center;
      margin-bottom: 24px;
    }
    .email-image img {
      width: 80px;
    }
    .resend {
      font-size: var(--sm);
    }
    .resend span {
      color: var(--very-light-pink);
    }
    .resend a {
      color: var(--hospital-green);
      text-decoration: none;
    }
    .primary-button {
      background-color: var(--hospital-green);
      border-radius: 8px;
      border: none;
      color: var(--white);
      width: 100%;
      cursor: pointer;
      font-size: var(--md);
      font-weight: bold;
      height: 50px;
    }
    .login-button {
      margin-top: 14px;
      margin-bottom: 30px;
    }
    @media (max-width: 640px) {
      .logo {
        display: block;
      }
    }
```
<br>

  ### Responsive Design
Our project is responsive, meaning it adapts to different screen sizes. To achieve this, we implemented media queries.
```
@media (max-width: 640px)
```

The styles outside apply to desktops, while those inside will apply when the viewport is smaller than 640 pixels.

There's another approach to responsive design, known as Mobile First. In this approach, you first think about styles for mobile devices and then gradually scale up to larger screens.


<br>
<br>

  ## Login

<br>
<br>

  ## Create and Edit my Account

<br>
<br>

  ## My Account

<br>
<br>
<br>

# RESPONSIVE LAYOUT: MAIN VIEWS
  ## Home Page: HTML

<br>
<br>

  ## Home Page: CS

<br>
<br>

  ## Desktop Menu

<br>
<br>

  ## Mobile Menu

<br>
<br>

  ## My Purchase Order: HTML

<br>
<br>

  ## My Purchase Order: CSS

<br>
<br>

  ## My Orders

<br>
<br>

  ## Navbar: HTML

<br>
<br>

  ## Navbar: CSS

<br>
<br>

  ## Product Details

<br>
<br>

  ## Shopping Cart: HTML

<br>
<br>
<br>

# NEXT STEPS



<br>
<br>
<br>

# AUTHOR

This project was developed by *Juan Cumbe*. If you have any questions or suggestions about the project, feel free to contact me via [e-mail](mailto:hello@juancumbe.com) or my [Linkedin](https://www.linkedin.com/in/juancumbeq/) profile. 