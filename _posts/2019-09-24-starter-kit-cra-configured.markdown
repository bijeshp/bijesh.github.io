---
layout: post
title:  "Starter Kit: A fully configured Create React App "
date:   2019-09-24 14:33:48 -0700
categories: starter-kit
---
You might find a number of starter-kits/boilerplate templates to bootstrap and application. The CRA starter kit is an extension of [Create React App](https://github.com/facebook/create-react-app) with necessary configuration and tool support

It uses following tools and technologies from the react ecosystem.

## Technologies and Libraries
- Application State : Redux
- Async Data Management : Redux Saga
- Declarative Routing : DOM bindings for React Router react-router-dom
- Static Type Checking :Flow
- REST API handling :Axios

## Setting up the Starter Kit
Download the starter-kit source files from the following [link](https://github.com/bijeshp/starter-kit-create-react-app.git)
`https://github.com/bijeshp/starter-kit-create-react-app.git`

## Code Organization

<img width="831" alt="Screen Shot 2019-09-24 at 3 14 52 PM" src="https://user-images.githubusercontent.com/7260229/65555185-b3143f80-dee0-11e9-92ea-47f90fa4da83.png">

## Developing with the Starter Kit

Basic Conventions
### 1. Modules :
A module is a logical grouping of related functionality, which maintain a namespace for data , routes and other related functionalities. A module typically contains the following parts
#### Pages
Defines a Container component and mounted on a route, Pages are the only connected components in a module. Data will be passed to the child components via props.All the page level components are defined in the components folder of each page.
Note : Its import to connect the reqStatus, isLoading,serviceError properties in each page as standard which helps to handle application state during the asynchronous data fetching.
#### index.js
Index.js of the module exports all the pages in the module. For example
#### routes.js
routes.js registers the routing for the module pages and the respective components to be mounted on the routes. For example
#### reducer.js
This defines the module reducer. Every reducer must contain following properties as default which helps to handle the application state during the asynchronous data fetching
#### actions
The *action.type.js *file defines the constants for all action types of the modules and the index.js file in the action directory defines all the actions for the module Note: If required actions can be grouped and separated in different module and then imported and exported form the index file .
#### sagas
Since we use redux saga middleware for asynchronous data handling , the module level sagas are specified in the sagas folder.the index file in sagas export all sagas belongs to the module.

### 2.Adding / Registering a New Module
When ever we add a new block/module of functionality to the application , It needs to be registered with the root application. The advantage of using this approach is each module level functional aspects are grouped into a module folder and in future if the application complexity increases and the module has to be separated into a new project is will easy to separate out.

### 3.Registering Module Routes to the application
The index file in the /src/routes/ directory imports and registers all the module level routes to the root application. It is important to note that AppBaseRoutes has to be placed always at last to handle non matching routes and error pages.

### 4.Registering Module Reducer to the application store
#### Registering Sagas
The sagas file in the /src/store/ directory imports and registers all the module level sagas to the root application.The module level sagas must be imported and added to the application sagas.

#### Registering Reducer
The reducers file in the /src/store/ directory imports and combines all the module level reducers to the root application.The module level reducers must be imported and added to the combineReducers method in the application reducer.

