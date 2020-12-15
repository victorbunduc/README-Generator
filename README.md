# README Generator:

## Description 
  

  Every  project needs a quality README with information about the app - what the app is for, how to use the app, how to install it, how to report the issues, and how to make contributions.


## Table of Contents
* [Installation](#installation)
* [Usage](#usage)
* [License](#license)
  

## Installation

*Steps required to install project and how to get the development environment running:*

To generate your own README, first run `npm install` in order to install the following npm package dependencies as specified in the `package.json`:
  * [`inquirer`](https://www.npmjs.com/package/inquirer) that will prompt you for your inputs from the command line 
  * [`axios`](https://www.npmjs.com/package/axios) to fetch your info from the GitHub API

The application itself can be started with `node index.js`.


## Usage 

*Instructions and examples for use:*

![Gif demo of README-generator](readme-demo.gif)

When you run `node index.js`, the application uses the `inquirer` package to prompt you in the command line with a series of questions about your GitHub and about your project.

The application then takes your responses and uses `axios` to fetch your GitHub profile from the [GitHub API](https://developer.github.com/v3/), including your GitHub profile picture and your email adress.
From there, the application will generate markdown and a table of contents for the README conditionally based on your responses to the Inquirer prompts.

Finally, `fs.writeFile` is used to generate your project's README.md file. 

## License

MIT License

---

