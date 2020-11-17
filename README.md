# Node Express

A guide to using Node to code

## Implement Node in a Directory
From the terminal, once inside the directory for the repository, run this line of code to turn it into a Node directory:
```
npm init
```

This will allow you to set up the JSON file (`package.json`) for the directory.

Be sure to create an `index.js` file (or whatever you designated as the main file in your `package.json` file).

## Create Node Modules
Add JS files, and fill them up with code. These should be reference files that you don't want to interact with on a regular basis but whose content you do want to easily access whenever necessary.

## Export Node Modules
If you want to export the entire contents of a module, you don't need to alter its content, as long as the module is a part of the directory in which you wish to use it.

To export only a part of a module, insert this code into the footer of the module:
```javascript
module.exports = {
    // methods
}
```

## Import Node Modules
To import an entire module into a file, insert this code into the header of the file:
```javascript
const module = require('module')
```

In the above example, the word `module` should be replaced with the name of the module being imported. You should also put `./` before the `module` in parentheses if the module being imported is from the current directory.

To import only a part of a module into file, change the header to this:
```javascript
const { /* methods */ } = require('module')
```

## Finding Node Modules
Use a resource like [NPMJS](https://www.npmjs.com/browse/depended) to find useful modules to import.

Read the modules documentation to determine how to install and use it. Most modules can be installed via the terminal. After intalling the module, make sure to import it into the file.

## Ignore Node Modules
To ensure that GitHub doesn't import your local copies of Node modules, add a `.gitignore` file to the project's repository. The only content of the file should be `node_modules`, which ensures that none of the third-party modules imported will uploaded when the project is pushed to GitHub.

## Using Node
In the terminal, run the code for a Node repository by typing `node index.js` (or `nodemon` if Nodemon is installed).

## Set Up Express
```
npm i express
```

## Create Route within Express
Header:
```javascript
const app = express()
```

## Sending Text from Server Back to Client
```
npm i ejs
```

Header:
```javascript
app.set('view engine', 'ejs')
```

## Sending HTML to the Client Using a View Template
```javascript
app.get('/', function(req, res) {
    res.render('index')
})
```

## Referencing Variables in a View Template
```html
 <h1>We're gonna count to ten:</h1>
 <% for (let i =1; i<11; i++){ %>
     <p><%= i %></p>
 <% } %>
 ```

## Creating Partials
These let you insert text chunks into pieces of various web pages, and if you change them in one place, they will render changes in all other places where they are located. This facilitates DRY code.

 ## Creating Layouts
 While partials act on a sub-level, layouts act on a super-level. They allow you to modify the appearance of the entire visual layout of every page (or set of pages) on a website. Instead of inserting partials everywhere, layouts allow you to establish a single design that will wrap around every subsequent page. This facilitates even DRY-er code.

 ## Creating Controllers
 These help you break out functionality by type. They take the site and break it up into chunks, with certain chunks being controlled by one controller and certain other chunks controlled by another controller.