# React: Getting started

## Requirements
You will need an installation of node and npm. Both are used to manage libaraies you will needalong the way. Node packages can be libraries or whole frameworks.

**Libraries** target a specific functionality, while a **framework** tries to provide everything required to develop a complete application. A framework inverts the control of the program. It tells the developer what they need. A library doesn’t. The programmer calls the library where and when they need it.

**Node Package Manager (npm)** allows you to install extermal **node packages** from the command line.

To check if you have node and npm installed, you can check which version you have.

```
node --version
*v8.9.4
npm --version
*v5.6.0
```

### How to intialize a npm project
```
npm init -y
```

`-y` uses the deafults in your package.json. If you don't use `-y`, then you'll have to decide how to configure hte file.

### Installing node packages

```
npm install <package>
npm install -g <package>
```

`-g` tells npm to install the pacakge globally

Since React is a package:
```
npm install React
```

The installed pagkage will automticalllly appear in a folder called _node_modules/_ and will be listed in teh _package.json_ file.

If you're working on someone else's project, you can use `npm install` in the command line, and that will install all the packages used in the project by taking all the dependenices listed in teh package.json file and installs them in the mode_modules/ folder.

Using a package for testing (use if node package is only used in a dev environment)
```
npm install --save-dev <package>
```

## Zero-Configuration Setup

```
npm install -g create-react-app
```

You can check the version of `create-react-app` to verify a successful installation

```
create-react-app --version
*v1.5.1
```

Bootsrap your first React app

```
create-react-app <name of app>
cd <name of app>
```

The folder stucture should be like this:

```
<name of app>
  README.md
  node_modules/
  package.json
  .gitignore
  public/
    favicon.ico
    index.html
    manifest.json
  src/
    App.css
    App.js
    App.test.js
    index.css
    index.js
    logo.svg
    registerServiceWorker.js
```

`node_modules/`: This folder has all the packages that were and are installed via npm. Usually do not need to touch this folder, but only install and uninstall node packages with npm from the command line.
`package.json`: Shows yo ua list of node package dependencies and other project configurations
`.gitignore`: Indicates all files and folders that shouldn't be added to your remote git repository when using git. They should only live in your local project. The `node_modules/` folder is a use case.

Other command lines to know

```
// Runs the application in http://localhost:3000
npm start

// Runs the test
npm test

// Builds the application for production
npm run build
```

The scripts are defined in `package.json` file.





