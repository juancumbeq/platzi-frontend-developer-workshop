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
  <img src="https://github.com/juancumbeq/platzi-frontend-developer-workshop/blob/main/readme_images/shopping-cart.png?raw=true" width= "40%" alt="Shopping Cart">
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
  ## Create New Password: HTML

  <br>
  <br>

  ## Create New Password: CSS

  <br>
  <br>

  ## Mail sent

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