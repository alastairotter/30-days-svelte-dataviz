# 30 days of Svelte, D3.js & data visualisation

---

##### - [Day 1 - Setting up Svelte](#day1)

---

<!-- ### Plan

Every day in December 2021 I plan to write a small piece about using [Svelte](https://svelte.dev/) and [D3.js](https://d3js.org/) to create data visualisations. On day 1 we'll start by installing Svelte and getting our basic project running. Each day after that we'll add more elements to our setup until we have a presentable chart.

In doing this I hope that I can learn more about the process (and document it) for myself and perhaps share some ideas. -->

### What is Svelte?

Svelte is a relatively new Javascript framework/library that helps build Javascript-based websites and apps. Working in Svelte will feel familiar to anyone that has used a framework like Vue.js or React. The difference with Svelte is that before we make our code public we compile it into its final form and then only publish the compiled code and none of the Svelte framework code. Sounds tricky but it's not.

**Resources**: Svelte has an excellent, [interactive tutorial site](https://svelte.dev/tutorial/basics).

### What is D3?

D3.js is a Javascript library that can be used to build interactive web elements and charts. In this series we'll make charts that are built on SVG, or scalable vector graphics which D3 is extremely flexible but it can be complicated to learn. D3 does not have pre-built charts like other tools such as [Flourish](https://flourish.studio) and [Datawrapper](https://datawrapper.de) which means it needs more work to start but the options are andless.

**Resources**: The [D3 gallery](https://observablehq.com/@d3/gallery) has examples of graphics created using D3.js

### Why Svelte and D3.js?

There are many reasons for combining D3 and Svelte but the biggest is that they complement each other really well. In this series we'll look at how to take the best of D3 and the best of Svelte to make something amazing. (More reasons may follow but for noe that will do).

## Prerequistites and preparations

This project assumes you have [Node.js](https://nodejs.org/) installed and you're reasonably familiar with Node, HTML, CSS and Javascript. You'll also need NPM, the Node package manager. Familiarity with D3.js and Svelte (or another Javascript framework) is beneficial.

There are mny different ways of installing Node and NPM depending on your platform. Most methods are linked from [Node.js](https://nodejs.org/).

Also recommended: [Visual Studio Code](https://code.visualstudio.com/) for editing the code.

**Resources**

- [Installing Nodejs: Tutorial: macOS](https://nodesource.com/blog/installing-nodejs-tutorial-mac-os-x/)

_**To Add**: Link/s to guides to install Node and NPM_
_**Questions**: Is NPM installed by default during Node installation?_

---

<span id="day1"></span>

# Day 1 - Setting up Svelte

The first thing we need to do is to install Svelte and set up a Svelte project. The quickest way to do this is to use a Svelte template.

### 0 - Using the terminal

You will need to run the following setup commands in the terminal on your computer. Depending on your platform there are various options. On Mac you can use the [built-in terminal app](https://www.howtogeek.com/682770/how-to-open-the-terminal-on-a-mac/). On Windows you can use the [built-in Command Prompt app (CMD)](https://www.webucator.com/article/how-to-run-a-nodejs-application-on-windows/). On Linux you can search for the "terminal" app and run that.

**Resources**

- [A quick guide to using commmand line (terminal)](https://towardsdatascience.com/a-quick-guide-to-using-command-line-terminal-96815b97b955)

### 1 - Checking/installing prerequisites

We'll assume you already have Node installed. To check this you can run:

    node -v

This should return the version number of node you have installed, like:

    v14.15.1

You'll also need `npx`. To check if you have that installed you can run:

    npx -v

This should return a version number if you have it installed. If you don't have `npx` installed you can install it by running:

    npm install npx

### 2 - Clone the Svelte template

With `node`, `npm` and `npx` installed you can now set up Svelte. The easiest way is to use `npx` to clone a template:

    npx degit sveltejs/template <name-of-project>

Replace `<name-of-project>` with a suitable directory name. (**Tip**: avoid using spaces in directory names. You can replace spaces in names with hyphens or underscores like: `my-project` or `my_project`)

Once you've done that you will have Svelte installed. To finish this process, switch to the new directory:

    cd <name-of-project>

... and install the dependencies:

    npm install

Your Svelte project should be installed and ready to view.

### 2 - Open your project in a code editor

[Visual Studio Code](https://code.visualstudio.com/) is recommended for editing code but, no matter which editor you're using, launch it and open the folder/directory you made earlier, the `<name-of-project>` directory.

When you open the folder in your editor you should see a file structure something like this in the sidebar:

![file structure](/public/images/file-structure.png)

> By default Svelte will set up a structure someting like this. To simplify things we'll put most of our code in the `src` directory. The only other directory worrying about at this stage is the `public` directory which is where the index.html file is stored as well as where we'll store some css files and images.

### 4 - Open the Visual Studio Code terminal

Visual Studio Code has a built-in version of the terminal application. You can open this from the `View` menu:

![open terminal](/public/images/open-terminal.png)

The terminal will open below the main editing window and by default you will be in the directory you created above. From this point on you can run all commands in this window instead of the terminal you used before.

### 4 - View the default Svelete app

By default Svelte will use the `src/App.svelte` file as the starting page for most projects. If you open that page in your editor you should see a whole lot of starting code. To see what that looks like in your browser you can compile the code and start up a web server. To do this run this code in the Visual Studio Code terminal:

    npm run dev

When you run this there will be some activity and then, hopefully, you will see something to suggest your application is ready to be viewed. The output will look like below and if you (command or control) click on the link (probably http://localhost:5000) the project will open in the browser locally:

![npm run dev](/public/images/dev-build.png)

When you click on this your browser should open and the default Svelte page will open.

### 5 - Stop the server

To stop (or restart) the server you can go back to the terminal in Visual Studio Code and use `control-c` to stop the process.

### 6 - Replace the App.svelte code

To get started we can delete the code in the `src/App.svelte` file and replace it with your own code.

Open the `App.svelte` file in VS Code and delete everything in that file. Then paste the following code into the `App.svelte` file:

    <script></script>
        <div>
            <h2>
            30 Days of Svelte and D3.js
            </h2>
        </div>
        <style>
        </style>

> **Svelte file structure** If you look at the code above it is a typical structure for Svelte files. Svelte files typically include three main elements: a `<script/>` section, an `HTML` section, and a `<style/>` section.

### 7 - Test our setup

To make sure things are working as expected you can run the dev server to compile our new code and start the server.

    npm run dev

Again, click on the http://localhost:5000 (or type that into your browser) to view your new page.

---

# Coming up

#### Day 2 - Adding local CSS styles

#### Day 2 - Adding and using components

#### Day 3 - Adding an SVG to your project and a shape

#### Day 4 - Moving the SVG to a component

#### Day 5 - Adding global CSS styles

#### Day 6 - Adding D3.js to your project
