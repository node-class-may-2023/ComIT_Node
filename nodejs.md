# Node.js

[<- Go Back](README.md)

* Node.js allows us to run JavaScript in different environments and run different tasks
* Using Node we can:
  * Run a simple script (like our exercises)
  * Bundle our front-end code and assets using different cool modules
  * Run a web server
  * Create back-end apps using different databases
* Over this course section we'll focus on using Node.js to create a web server and create a back-end app
* We'll create dynamic documents
* When we installed Node.js we also installed other program called NPM

## NPM
* NPM used to stando for Node Package Manager but now a day it's just NPM as name
* Thanks to NPM we can install many different Node.js modules and import them on our projects
* This way we reuse code and we can contribute to other modules too
* NPM is one of the largest modules repository 
* Visit [NPM site](https://www.npmjs.com) to learn more about it
* Also learn more reading [NPM blog](https://blog.npmjs.org)
* Also, they have the best mascot ever.. NPM wombat!!

![Wombat](./resources/images/node/wombat.png)

### Start a new NPM project
* To start a new project firs we need to create a new folder and change directory inside it
* You can do this in unix like systems

```
mkdir learning-node && cd learning-node
```

* Once we're in the right folder we run the NPM command and init
* This command ask a lot of questions to configure our project
* We can ignore them and just press enter
* [NPM init doc](https://docs.npmjs.com/cli/init)

```bash
npm init
```

* Or we can generate it without having to answer the questions

```bash
npm init -y
```

* This script creates a new package.json file that allows us to configure our project
* Just looking at the file extension we can figure out that we'll use JSON for our npm configuration file

```js
{
  "name": "learning-node",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "author": "",
  "license": "ISC"
}
```

* NPM init uses our answers to create the configuration file based on our answers
* Once we have the file we can update any value on it

### NPM scripts
* On the **package.json** file we can find a **sripts** key
* By default we have a test script
* We can create our own scripts
* Add a **start** script

```js
"scripts": {
  "test": "echo \"Error: no test specified\" && exit 1"
  "start": "node index.js"
},
```

* Now we can run this command from our command line

```bash
npm start
```

* At this point we get an error

```bash
Error: Cannot find module 'index.js'
```

* We get this error as we try to execute index.js script and node can't find it
* As we are calling `node index.js` we need to create this new file at the same package.json or root level
* Update the start script definition if you need to move index.js to a different project/folder structure
* Create index.js and add the following code

**index.js**
```js
console.log('Welcome to JavaScript and Node.js server side');
```

* Run the npm start command again

```bash
npm start

Welcome to JavaScript and Node.js server side
```

* Now we know how to create, configure and run scripts using NPM and Node

### Install NPM module
* Using NPM we can install modules and use them on our projects
* Run **npm install** and the module name to install the given module
* You can check and search for modules on the [NPM site](https://www.npmjs.com)
* In this case we're going to install **Express** that's a popular module to create a web server
* Check out [express npm page](https://www.npmjs.com/package/express)
* Also, take a look at [express site and doc](http://expressjs.com)

```bash
npm install express
```

**package.json**
```js
"dependencies": {
  "express": "^4.16.3"
}
```

* Runnig NPM install creates a **node_modules** folder
* Inside **node_modules** we find all the installed modules for a given project
* This folder can grow in size as we can have many installed modules or dependencies
* To avoid having issues we can [.gitignore](https://git-scm.com/docs/gitignore) this folder
* So if we're not sharing the node_modules folder with other team members... do we need to remember the list of installed modules?
* By default now NPM installs the modules and add them to our package.json dependecies
* Delete the node_modules folder
* Run the npm install command but whitout the module name

```bash
npm install
```

* NPM reads our list of dependencies, downloads and install all the modules for us



### Using fetch and POST
* The `fetch` method accepts a second parameter
* This parameter is a JavaScript object with `request data`

* [MDN fetch doc](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API)
* [Youtube - Fetch API](https://www.youtube.com/watch?v=g6-ZwZmRncs)
* [Working with the Fetch API](https://www.youtube.com/watch?v=9Qtvjd0UbAs)
* [MDN promises doc](https://developer.mozilla.org/es/docs/Web/JavaScript/Referencia/Objetos_globales/Promise)
* [MDN Using promises guide](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Using_promises)
* [Youtube - How to Use Javascript Promises](https://www.youtube.com/watch?v=104J7_HyaG4)
* [Google Developers - JavaScript Promises: an Introduction](https://goo.gl/ZH6spE)