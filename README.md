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

  ## [Login](https://github.com/juancumbeq/platzi-frontend-developer-workshop/blob/main/project/3-login.html)

Now we will work on styling the login screen. This is where users will be able to access the application you are creating. You will also encounter a layout challenge that you can solve in the comments.

<p align="center">
  <img src="https://github.com/juancumbeq/platzi-frontend-developer-workshop/blob/main/readme_images/login.png?raw=true" width= "35%" alt="Login">
</p>

<br>

  ### HTML Code
As we can see in the image, we have a logo, two inputs, a button with text below it, and another button that in its mobile version moves to the bottom of the screen.
```
<div class="login">
  <div class="form-container">
    <img src="./logos/logo_yard_sale.svg" alt="logo" class="logo">

    <form action="/" class="form">
      <label for="email" class="label">Email address</label>
      <input type="text" id="email" placeholder="platzi@example.cm" class="input input-email">

      <label for="password" class="label">Password</label>
      <input type="password" id="password" placeholder="*********" class="input input-password">

      <input type="submit" value="Log in" class="primary-button login-button">
      <a href="/">Forgot my password</a>
    </form>

    <button class="secondary-button signup-button">Sign up</button>
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
}
.logo {
  width: 150px;
  margin-bottom: 48px;
  justify-self: center;
  display: none;
}
.form {
  display: flex;
  flex-direction: column;
}
.form a {
  color: var(--hospital-green);
  font-size: var(--sm);
  text-align: center;
  text-decoration: none;
  margin-bottom: 52px;
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
.input-email {
  margin-bottom: 22px;
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
.secondary-button {
  background-color: var(--white);
  border-radius: 8px;
  border: 1px solid var(--hospital-green);
  color: var(--hospital-green);
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

  ### Types of positioning in HTML

Position can have any of these values:

<p align="center">
  <img src="https://github.com/juancumbeq/platzi-frontend-developer-workshop/blob/main/readme_images/position.png?raw=true" width= "60%" alt="Position">
</p>

  * **Static**: Default position of elements. It's the only case where top, right, bottom, and left cannot be used.

  * **Absolute**: Elements remain in the position where they were placed but lose their physical space, meaning they overlap other elements. Note: to apply this value, the parent container must have position relative.

  * **Relative**: Elements retain their original position and physical space, but we can move them with the top, right, bottom, and left properties.

  * **Fixed**: Elements lose their physical space and remain fixed in place.

  * **Sticky**: Elements retain their physical space, but when scrolled, they follow without losing that space. It's commonly used for navigation bars.

  * **Initial**: Returns the position of an element to its original state.

  * **Inherit**: Inherits the position from its parent.

<br>
<br>

  ## [Create and Edit my Account](https://github.com/juancumbeq/platzi-frontend-developer-workshop/blob/main/project/4-create-account.html)
We will layout the view that will allow the user to create or edit their account. This includes a title, three input fields for entering data, and a button.

<p align="center">
  <img src="https://github.com/juancumbeq/platzi-frontend-developer-workshop/blob/main/readme_images/create.png?raw=true" width= "45%" alt="Create">
</p>

<br>

   ### How to Layout a Registration Form
To layout this form, you can refer to the code generated for the login view. Remove the logo and subtitle from this structure, and it should look like this:
```
<div class="login">
    <div class="form-container">
        <h1 class="title">My account</h1>
        <form action="/" class="form">    
            <div>
                <label for="name" class="label">Name</label>
                <input type="text" id="name" placeholder="Teff" class="input input-name">

                <label for="email" class="label">Email</label>
                <input type="text" id="email" placeholder="platzi@example.com" class="input input-email">

                <label for="password" class="label">Password</label>
                <input type="password" id="password" placeholder="*********" class="input input-password">
            </div>
            <input type="submit" value="Create" class="primary-button login-button">
        </form>
    </div>
</div>
```

Finally, before the closing form tag, add the button so the user can submit the information.

<br>

   ### Styles for the Registration Form:
We'll add some more styles to the ones we used previously in the "new password" section to format this section.

Adjustments include:

  * Increasing the spacing between the form inputs:
```
  .input-name,
  .input-email,
  .input-password {
      margin-bottom: 22px;
  }
```
  * Modify the CSS of the "title" class to align the title to the left and distance it from the inputs:

```
  .title {
      margin-bottom: 36px;
      text-align: start;
  }
```
<br>

  ### How to Align the Form Button?
Similar to the previous challenge, in its mobile version, this screen moves the button away from the form by placing it at the bottom. One of the simplest and most effective ways to do this is by using Flexbox.

We start by giving our container and form a height of 100%. Since the form is already flexible and has a column direction, we just need to add in the media query: justify-content: space-between.

This property positions the content horizontally when the value of flex-direction is row. In our case, the value is columns, so justify-content will apply vertically.

Space-between distributes the items evenly, leaving the first item at the beginning and the last one at the end.

<br>
<br>

  ## [My Account](https://github.com/juancumbeq/platzi-frontend-developer-workshop/blob/main/project/5-my-account.html)
This time I'll teach you how to layout the screen that allows the user to edit their account. As you can see, this view contains other relevant data such as the email, password, and the person's name.

<p align="center">
  <img src="https://github.com/juancumbeq/platzi-frontend-developer-workshop/blob/main/readme_images/edit.png?raw=true" width= "45%" alt="Edit">
</p>

<br>

  ### How to Show the User the Entered Data
To show the user the data they entered during registration, we'll use the code from the "create account" section. Keeping in mind that the purpose of this view is to display information, not obtain it, we need to modify the form as follows:

  * We'll change the inputs to paragraphs:
```
<div>
    <label for="name" class="label">Name</label>
    <p class="value">Camila Yokoo</p>

    <label for="email" class="label">Email</label>
    <p class="value">camilayokoo@gmail.com</p>

    <label for="password" class="label">Password</label>
    <p class="value">*********</p>
</div>
```

  * Styling the text:
```
.value {
    color: var(--very-light-pink);
    font-size: var(--md);
    margin: 8px 0 32px 0;
}
```

  * Apply the secondary-button class to the button:
```
.secondary-button {
    background-color: var(--white);
    border-radius: 8px;
    border: 1px solid var(--hospital-green);
    color: var(--hospital-green);
    width: 100%;
    cursor: pointer;
    font-size: var(--md);
    font-weight: bold;
    height: 50px;
}
```
<br>

  ### How to Proceed With the Project
We have completed the module for creating authentication screens. Now, all that's left is to build the main views. Remember that in the Practical React.js Course, we will combine all the screens to finish our frontend.

<br>
<br>
<br>

# RESPONSIVE LAYOUT: MAIN VIEWS
  ## [Home Page: HTML](https://github.com/juancumbeq/platzi-frontend-developer-workshop/blob/main/project/6-home-page.html)
The homepage is the main web page of a website and the first thing people will see when they encounter your brand. In this case, it contains an image for each product, with its price and name, as well as an icon that allows users to add the item to the shopping cart.

In this new module, we will work on the main views. We start with the HTML for the homepage, i.e., the cards that help the user review the available products in an e-commerce.

<p align="center">
  <img src="https://github.com/juancumbeq/platzi-frontend-developer-workshop/blob/main/readme_images/cards.png?raw=true" width= "90%" alt="Cards">
</p>

<br>

  ### How to create the HTML Structure of the homepage:

These are the steps to follow to layout the sections of an e-commerce. Let's get started!

  * Create a main section: 
    * ```<section class="main-container"></section>```

  * Inside, place a div that will serve as a container for the cards, allowing us to center them:
    * ```<div class="cards-container"></div>```

  * Finally, structure a card and repeat it several times:
  * ```
    <div class="product-card">
        <img src="https://images.pexels.com/photos/276517/pexels-photo-276517.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940" alt="">
        <div class="product-info">
            <div>
                <p>$120,00</p>
                <p>Bike</p>
            </div>
            <figure>
                <img src="./icons/bt_add_to_cart.svg" alt="">
            </figure>
        </div>
    </div>
    ```

<br>

  ### How to Place Images in HTML:

The HTML img element embeds an image into a document. Its "src" attribute is used to specify where the image is located, whether in a folder or a URL.

Meanwhile, "alt" is used to add a description to our image. This is useful for SEO (search engine optimization) purposes and also improves site accessibility.

Review this information here 👈

<br>

  ### Which Containers to Use?

There are two tags that allow us to organize images in a semantic way.

  * [Figure](https://platzi.com/new-home/clases/2008-html-css/31081-etiqueta-figure/)
  * [Picture](https://platzi.com/new-home/clases/2008-html-css/31222-imagenes-responsive/)

<br>
<br>

  ## [Home Page: CS](https://github.com/juancumbeq/platzi-frontend-developer-workshop/blob/main/project/6-home-page.html)
Now we'll style the cards that make up the homepage using CSS Grid. Users will see different styles depending on the device they connect from, and here you can identify their differences.

Here's the visualization from a computer:

<p align="center">
  <img src="https://github.com/juancumbeq/platzi-frontend-developer-workshop/blob/main/readme_images/cards.png?raw=true" width= "90%" alt="Cards">
</p>

And this is the design for mobile devices:
<p align="center">
  <img src="https://github.com/juancumbeq/platzi-frontend-developer-workshop/blob/main/readme_images/cards-mobile.png?raw=true" width= "90%" alt="Cards Mobile">
</p>

<br>

  ### How to implement CSS Grid to center multiple images:
We'll work on the main container, whose class is "cards-container". Using "display: grid", we create the grids and then define the columns with "grid-template-columns", using the "repeat" function to repeat our code fragment.

Using "auto-fill", we ensure that the grid occupies 100% of the available space. Then, we generate space between the items with "gap". Finally, we align them horizontally and vertically using "place-content".

The CSS would look like this:

```
.cards-container {
  display: grid;
  grid-template-columns: repeat(auto-fill, 240px);
  gap: 26px;
  place-content: center;
}
```
Now we need to adjust the size of the images.

```
.product-card {
  width: 240px;
}
.product-card img {
  width: 240px;
  height: 240px;
  border-radius: 20px;
  object-fit: cover;
}
```

<br>

  ### Same class, different styles:

We want the cards on the homepage to display the item's price and below it, the name of the item with a different font size and color.

Next to both should be the shopping cart icon.

To achieve this result, we must:

Apply Flexbox to the container:

```
.product-info {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-top: 12px;
}
```
Adjust the size of the icon:

```
.product-info figure {
  margin: 0;
}
.product-info figure img {
  width: 35px;
  height: 35px;
}
```
Use nth-child on the p tags:

```
.product-info div p:nth-child(1) {
  font-weight: bold;
  font-size: var(--md);
  margin-top: 0;
  margin-bottom: 4px;
}
.product-info div p:nth-child(2) {
  font-size: var(--sm);
  margin-top: 0;
  margin-bottom: 0;
  color: var(--very-light-pink);
}
```
The nth-child pseudo-class allows us to apply different styles to the paragraphs without needing to assign a class to each one.

<br>

  ### Responsive homepage with just 8 lines of code:

By assigning media queries, we ensure that the cards look good on different screens, i.e., we develop a responsive homepage.

Since we implemented CSS Grid, all we need to do is reduce the size of the images, like this:

```
@media (max-width: 640px) {
  .cards-container {
    grid-template-columns: repeat(auto-fill, 140px);
  }
  .product-card {
    width: 140px;
  }
  .product-card img {
    width: 140px;
    height: 140px;
  }
}
```

<br>
<br>

  ## [Desktop Menu](https://github.com/juancumbeq/platzi-frontend-developer-workshop/blob/main/project/6-home-page.html)

<br>
<br>

  ## [Mobile Menu](https://github.com/juancumbeq/platzi-frontend-developer-workshop/blob/main/project/6-home-page.html)

<br>
<br>

  ## [My Purchase Order: HTML](https://github.com/juancumbeq/platzi-frontend-developer-workshop/blob/main/project/6-home-page.html)

<br>
<br>

  ## [My Purchase Order: CSS](https://github.com/juancumbeq/platzi-frontend-developer-workshop/blob/main/project/6-home-page.html)

<br>
<br>

  ## [My Orders](https://github.com/juancumbeq/platzi-frontend-developer-workshop/blob/main/project/6-home-page.html)

<br>
<br>

  ## [Navbar: HTML](https://github.com/juancumbeq/platzi-frontend-developer-workshop/blob/main/project/6-home-page.html)

<br>
<br>

  ## [Navbar: CSS](https://github.com/juancumbeq/platzi-frontend-developer-workshop/blob/main/project/6-home-page.html)

<br>
<br>

  ## [Product Details](https://github.com/juancumbeq/platzi-frontend-developer-workshop/blob/main/project/6-home-page.html)

<br>
<br>

  ## [Shopping Cart: HTML](https://github.com/juancumbeq/platzi-frontend-developer-workshop/blob/main/project/6-home-page.html)

<br>
<br>
<br>

# NEXT STEPS



<br>
<br>
<br>

# AUTHOR

This project was developed by *Juan Cumbe*. If you have any questions or suggestions about the project, feel free to contact me via [e-mail](mailto:hello@juancumbe.com) or my [Linkedin](https://www.linkedin.com/in/juancumbeq/) profile. 