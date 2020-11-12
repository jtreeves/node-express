# Node Shortcuts

From the terminal, once inside the directory for the repo, make it a node repo:
```
npm init
```

This will allow you to set up the JSON file

Code to put in the header of the main file in order to import aspects from the reference file:
```javascript
const { beBasic, add, subtract } = require('./myModule')
```

Code to put in the footer of the reference file in order to export its aspects to the main file:
```javascript
module.exports = {
    beBasic,
    add,
    subtract
}
```

Main file: `index.js`
Reference file: `myModule.js`

Names for files and functions obviously vary based on scenario
