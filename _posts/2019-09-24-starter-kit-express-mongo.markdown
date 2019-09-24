---
layout: post
title:  "Starter Kit : REST API development setup using express mongo and Mongoose"
date:   2019-09-20 14:33:48 -0700
categories: starter-kit
---
This is a modern boilerplate application for building REST ful APIs Micro-service in Node.js using express and mongo DB mongoose in ES6 with code coverage and other developer tools. 

This boiler plate [template](https://github.com/bijeshp/starter-kit-express-mongo-api) has following tools and technologies setup for easy development

## ES6 Support Using ESM

Most of the commonly used ES6 features are supported by Node version 10.15.3, ES6 module loading specifications are not yet a standard in the node version. ESM is a module loader that transforms es modules at run time instead of transpiling them.(Typically we use babel for command line transpiling ES6 code to ES5)

## Code Quality
**Code Formatting** - Code formatting is done using [Prettier](https://prettier.io/)  
**Pre-commit hooks** - [Husky](https://github.com/typicode/husky#readme) Ensures the code is formatted as per the development standard for every commit

## Code Instrumentation

[Istanbul](https://github.com/istanbuljs/nyc#readme) instruments your ES5 and ES2015+ JavaScript code with line counters, so that we can track how well your unit-tests exercise your codebase.The nyc command-line-client for Istanbul works well with most of the javascript frameworks.

### Documentation

jsdoc has been used for API documentation
To set this locally install jsdoc globally or as a dev dependency as part of the setup

`npm install -g jsdoc`

Run the following command to generate documentation for the code base
`yarn build-docs`
Run the following command to generate documentation for a single file (yourJavaScriptFile)

`jsdoc yourJavaScriptFile.js`

### Unit Testing

Chai and Mocha are used for writing unit test cases  
Assertion with Chai provides natural language assertions, expressive and readable style.

## Developing With Starter Kit
Checkout the code from following git repo to start developing with the template

`https://github.com/bijeshp/starter-kit-express-mongo-api.git`

## Code Organization

<img width="663" alt="Screen Shot 2019-09-24 at 3 50 07 PM" src="https://user-images.githubusercontent.com/7260229/65556455-8d893500-dee4-11e9-926c-e32d2e2890b2.png">

Read more about setting up and running the application [here](https://github.com/bijeshp/starter-kit-express-mongo-api/edit/master/README.md).