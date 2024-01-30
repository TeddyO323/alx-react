# Project Title

## Webpack Configuration for Front-end Development with ES6

![Holberton Logo](images/121b1f6534e60566e1de.png)


### Table of Contents

- [Introduction](#introduction)
- [Resources](#resources)
- [Learning Objectives](#learning-objectives)
- [Requirements](#requirements)

## Introduction

This project focuses on configuring Webpack for front-end development using JavaScript with ES6 features. The following key concepts will be covered:

- Setting up Webpack for a basic project
- Understanding entry points, output, and loaders
- Incorporating plugins into the Webpack configuration
- Code splitting techniques
- Configuring a development server for an efficient workflow

## Resources

Read or watch the following resources to gain a better understanding:

- [Webpack Documentation](https://intranet.alxswe.com/rltoken/XEFTUAcZ_9sKurp1Bui7ug)
- [Webpack Beginner Guide](https://intranet.alxswe.com/rltoken/6ngQzrV7xeKJjcRwdmrYAQ)
- [npm-package.json](https://intranet.alxswe.com/rltoken/P00rJM5qCeaf33hsPuhgog)

## Learning Objectives

By the end of this project, you should be able to explain the following concepts without relying on external resources:

- Setting up Webpack for a basic project
- Understanding and configuring entry points, output, and loaders
- Adding plugins to enhance Webpack functionality
- Implementing code splitting strategies
- Configuring and utilizing a development server

## Requirements

Ensure that your code adheres to the following requirements:

- Execution on Ubuntu 18.04 LTS using Node 12.x.x
- Allowed editors: vi, vim, emacs, Visual Studio Code
- All files should end with a new line
- A mandatory README.md file should be present at the root of the project folder.

--- 

# Tasks

## Task 0: Basic setup (100% Completed)

**Objective:** Create and run Webpack using a basic installation.

Tasks:

0. Basic setup
   - **Status:** 100% Completed
   - **Score:** 100%
   - **Checks completed:** 100%
   - **Details:**
     - Create a folder named `task_0`.
     - Install webpack and webpack-cli as developer dependencies within the folder using npm.
     - Install jQuery as a regular dependency using npm.
     - Ensure that webpack and webpack-cli are listed under the `devDependencies` key, and jQuery is listed under the `dependencies` key within `package.json`.
     - Create a `src` directory with an `index.js` in it. The file should import jQuery and add three different paragraphs to the page body.
     - Create a `dist/index.html`. Import your `main.js` in the body. Use jQuery to add elements to the body of the page.
     - When running Webpack, your JavaScript and HTML files should be generated in a `dist` folder.
     - Do NOT push your `dist/main.js` if you have one.

Repo:

- GitHub repository: `alx-react`
- Directory: `0x00-Webpack`
- File: `task_0`/`package.json`, `task_0`/`src`/`index.js`, `task_0`/`dist`/`index.html`

---

## Task 1: Learning how to use Webpack with a config file (100% Completed)

**Objective:** Installing packages and using jQuery.

Tasks:

1. Learning how to use Webpack with a config file
   - **Status:** 100% Completed
   - **Score:** 100%
   - **Checks completed:** 100%
   - **Details:**
     - Create a folder named `task_1`, cd into it, and create a `package.json` using `npm init -y`.
     - Install webpack (dev dependency), jQuery (dependency), and Lodash (dependency) within the folder using `npm`.
     - Modify your `package.json` to add a build script that runs webpack to create a production build. This lets you execute `npm run build` on the command line.
     - Create a `js` directory with a JavaScript file named `dashboard_main.js` in it. The file should import jQuery and add elements to the page.
     - Write a function called `updateCounter()` that tracks the number of times a button element has been clicked. Each time it's called, update the count by 1 and set the content of a paragraph element with id='count' to `{count} clicks on the button`.
     - Set Webpack config mode to production.
     - Opening your HTML file should not generate any error in the console.

Repo:

- GitHub repository: `alx-react`
- Directory: `0x00-Webpack`
- File: `task_1`/`js`/`dashboard_main.js`, `task_1`/`package.json`, `task_1`/`webpack.config.js`, `task_1`/`public`/`index.html`

---

## Task 2: Adding CSS & Images (100% Completed)

**Objective:** Create a specific configuration for Webpack.

Tasks:

2. Adding CSS & Images
   - **Status:** 100% Completed
   - **Score:** 100%
   - **Checks completed:** 100%
   - **Details:**
     - Create a specific configuration for Webpack using the folder named `task_2`.
     - Reuse the code from `task_1`.
     - Modify the webpack config to support adding CSS to the bundle.
     - Modify the webpack config to support adding images to the CSS.
     - Create a `css` folder. In a file named `main.css`, change the position of the counter text and add an element at the top of the document with the id `#logo` which has a width of 200px and height of 200px. Set the background of the element with the image in `task_2/assets/holberton-logo.jpg`.
     - Configure Webpack to optimize images.
     - When running Webpack, your JavaScript and HTML files should be generated in a `public` folder.
     - Opening your main file should not generate any error in the console.
     - Your HTML code should only import one JavaScript script (the one generated by webpack).
     - When running Webpack, you should not see the warning `WARNING in asset size limit: The following asset(s) exceed the recommended size limit`.

Repo:

- GitHub repository: `alx-react`
- Directory: `0x00-Webpack`
- File: `task_2`/`package.json`, `task_2`/`css`/`main.css`, `task_2`/`webpack.config.js`, `task_2`/`js`/`dashboard_main.js`, `task_2`/`public`/`index.html`

---

## Task 3: Dev servers, modules, and tree shaking (100% Completed)

**Objective:** Set up a development server, divide code into modules, and optimize bundles size.

Tasks:

3. Dev servers, modules, and tree shaking
   - **Status:** 100% Completed
   - **Score:** 100%
   - **Checks completed:** 100%
   - **Details:**
     - Set up a development server in the folder named `task_3`.
     - Reuse code from `task_2`.
     - Modify the Webpack config to set up a development server running on port 8564.
     - Set the mode to development in the Webpack config.
     - Add a script in `package.json` to start the server and open the browser with `npm run start-dev`.
     - Divide the main bundle into three modules:
       - `header`: Contains `header.css` and `header.js` files. Import jQuery, add logo and H1 title to `header.js` with content "Holberton Dashboard", and add a console.log printing "Init header". Add necessary styles to `header.css`.
       - `body`: Contains `body.css` and `body.js` files. Import jQuery, Lodash, and add the body code (button, counter) in `body.js`. Add necessary styles to `body.css`.
       - `footer`: Contains `footer.css` and `footer.js` files. Import jQuery and append a paragraph with the copyright text "Copyright - Holberton School". Add necessary styles to `footer.css`.
     - Modify the Webpack configuration to support three different entry points (`header`, `body`, `footer`). Each entry point should generate a filename with the format `name_of_the_file.bundle.js`.
     - Do NOT have a `task_3/public/` directory pushed to your repository.
     - Add a plugin to Webpack to automatically create an `index.html` HTML file.
     - Improve development speed:
       - Modify the Webpack config to support inline source mapping.
       - Check that the `console.log` in `header.js` now takes you to your JavaScript file instead of the main bundle.
       - Add a plugin to Webpack to clean your build folder on each build.
     - Improve bundles size:
       - Modify the Webpack configuration to split the modules into chunks.

Repo:

- GitHub repository: `alx-react`
- Directory: `0x00-Webpack`
- File: `task_3`/`modules`/`body`/`body.css`, `task_3`/`modules`/`body`/`body.js`, `task_3`/`modules`/`footer`/`footer.css`, `task_3`/`modules`/`footer`/`footer.js`, `task_3`/`modules`/`header`/`header.css`, `task_3`/`modules`/`header`/`header.js`, `task_3`/`package.json`, `task_3`/`webpack.config.js`

---


