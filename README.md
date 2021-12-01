# 30 days of Svelte and data visualisation

### Plan

Every day in December 2021 I plan to write a small piece about using [Svelte](https://svelte.dev/) and [D3.js](https://d3js.org/) to create data visualisations. On day 1 we'll start by installing Svelte and getting our basic project running. Each day after that we'll add more elements like D3.js, creating components for each of the charts, and adding some styling so our charts look good.

In doing this I hope that I can learn more about the process for myself and perhaps share some ideas.

### What is Svelte?

Svelte is a relatively new Javascript framework/library that helps build Javascript-based websites and elements.

### What is D3?

D3.js is a Javascript library that can be used to build interactive web elements and charts. D3 is extremely flexible but it can be complicated to learn. D3 does not have pre-built charts like other tools like [Flourish](https://flourish.studio) and [Datawrapper](https://datawrapper.de) which means it needs more work to start but the options are andless.

### Why Svelte and D3.js?

There are many reasons for focusing on these two tools/frameworks but they all boil dow to the simple fact that Svelte and D3.js work together excellently and make producing most charts relatively easy. (More reasons may follow but for noe that will do).

### Prerequistites

This project assumes you have [Node.js](https://nodejs.org/) installed and you're reasonably familiar with Node, HTML, CSS and Javascript. You'll also need NPM, the Node package manager. Familiarity with D3.js and Svelte (or another Javascript framework) is beneficial.

There are mny different ways of installing Node and NPM depending on your platform. Most methods are linked from [Node.js](https://nodejs.org/).

---

### 1 December 2021 - Setting up Svelte

The first thing to do is set up a Svelte project.

The quickest way to do this is to use a Svelte template.

##### 1 - Clone the Svelte template

At the terminal run the following:

    `npx degit sveltejs/template <name-of-project>`

**Note**: If you get an error, you may need to install `npx` first. You can do this by running:

    `npm install npx`

Once you've done that you will have Svelte installed. To finish this process, switch to the new directory:

    `cd <name-of-project>`

And then the install the dependencies:

    `npm install`

This will create a file structure something like this:

![file structure](/public/images/file-structure.png)

##### 2 - Create a folder for components

You can create this most places but for this project create the folder in the `src` directory:

    `mkdir components`

##### 3 - Set up yhe App.svelte file

By default the App.svelte file will have some basic code in it. You can delete all of this and replace with this minimal code:

    <script></script>
        <div>
            <h2>
            30 Days of Svelte and D3.js
            </h2>
        </div>
        <style>
        </style>

In Svelte, like most other Javascript frameworks, files or components usually contain three main elements: a `<script/>` section, an `HTML` section and a `<style/>` section.

##### 4 - Test out setup

To make sure things are working as expected you can run the dev server which will compile the Svelte code:

    `npm run dev`

When you run this it will prepare the dev server. The output will look like this and if you (command or control) click on the link (probably http://localhost:5000) the project will open in the browser locally:

![npm run dev](/public/images/dev-build.png)

When you click on the dev server link you should see the HTML version of the code we added to App.svelte earlier.

---

# Coming up

### December 2 2021 - Adding an SVG to your project and a shape

### December 3 2021 - Moving the SVG to a component

### December 4 2021 - Svelte and CSS

### December 5 2021 - Adding D3.js to your project
