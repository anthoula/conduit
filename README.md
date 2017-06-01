Conduit : A Medium.com clone
----------------------------

## Overview

Learn React / Redux and Node.js by a real-world practice project.

## Objective

Create a production ready Medium.com clone called "Conduit" powered by my choice of frontend & backend frameworks. I've chosen React / Redux and Node.js. Live demo of the application [here](https://demo.productionready.io/#/).

## Anatomy of an Express Application

The project's directory structure is based off of the one created by the [express-generator](https://expressjs.com/en/starter/generator.html).

## Structure
.
├── config/
│   └── index.js
├── models/
├── public/
├── routes/
│   ├── api/
│   │  └── index.js
│   └── index.js
├── app.js
├── package.json
└── .gitignore

* The `config` folder will be used for storing configuration settings for our application. For our project, we'll be storing our environment variables and configuration for passport.js in this folder.
* The `models` folder will be used for storing our Mongoose models. These models will contain the schema for our data and will be the entry point for how our data gets in and out of MongoDB.
* The `public` folder is used for storing static files to be served, such as HTML, CSS, and Javascript files. Since we're only concerned about building an API, this folder won't be used in this tutorial, but if build a client application for this project later it can live in this folder.
* The `routes` folder is where we define the routes that our application will respond to and will contain the logic for our endpoints.
* `app.js` is the entry point into our application. This is the file that `node` will execute and will bring together all parts of our application (routes, models, etc).
* The `package.json` file is used by `npm` for declaring our dependencies and scripts for our application. You can read more about the different configuration options that can go into `package.json` [here](https://docs.npmjs.com/files/package.json)

## Tools
- `Express` - for server logic. (https://expressjs.com/)
- `MongoDB` - our data will be stored in MongoDB. MongoDB is a NoSQL database which stores data in collections and documents (as opposed to tables and rows in SQL).
- `mongoos.js` - Library we will use for all of our interactions with MongoDB. Mongoose allows us to to define schemas and indices for our database, as well as providing callbacks and validations for ensuring our data remains consistent. Mongoose also has a plugin system for reusing code between schemas or importing community libraries to extend the functionality of our models.
- [nodemon](https://github.com/remy/nodemon) - command line tool that automatically monitors the folder of our project and reboot our server for us whenever it sees a file change. This has been added to `package.json` as an NPM script to start the server in development

## Local Development

1. Boot up MongoDB database (leave tab running in background)
```
mongod
```

2. Start the Node server via NPM
```
npm run dev
```
You should then see a message similar to the following, which means your server booted up successfully, and you're ready to start coding!
```
[nodemon] starting `node app.js`
Listening on port 3000
```

## Checklist

I'll be building out each feature in our application in three phases:

- [ ] Create the mongoose Models
- [ ] Create any helper methods on our models and route middleware required for the feature
- [ ] Creating the route to expose the functionality to our users
