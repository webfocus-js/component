<p align="center">
    <img src="https://raw.githubusercontent.com/diogoalmiro/webfocus/main/static/favicon.svg" alt="Webfocus Logo" height="90">
</p>

# Webfocus

This module defines the WebfocusComponent class to help in the creation of NodeJS servers using [express](https://expressjs.com/) and [Pug](https://pugjs.org/).

The main idea of this module is to enable the creation of independet components with the `WebfocusComponent` class and the creation of applications with `WebfocusApp` class [(see @webfocus/app)](https://www.npmjs.com/package/@webfocus/app) using said components.

Specifically, the `WebfocusComponent` represents a specific component.
To create a new component `const webfocusComponentInstance = require('@webfocus/app/component')(name: String, description: String)`.
Or access the class with `const WebfocusComponent = require('@webfocus/app/component').WebfocusComponent` with the constructor `new WebfocusComponent(name: String, description: String, dirname: String);`.
[More information of WebfocusComponent.](https://github.com/webfocus-js/component/blob/main/doc/webfocus-component.md)

## Getting Started

On your current project:

`npm install @webfocus/component`

Or use the initializer:

`npm init @webfocus/component`

The later will create a template WebfocusComponent (the `package.json`, `index.js` and `index.pug` files)

## Usage

```javascript
let component = module.exports = require('@webfocus/component')("Component Name", "Component Description");

component.app.get('/', (req, res) => {
    res.json("Hello World from this component!");
})
```

In the [repository](https://github.com/diogoalmiro/webfocus-cypress-tests) we do end-to-end tests with cypress tests on an sample implementation.

## TODO
 
 - Create an WebfocusComponent addon to enable distribution of a heavy process
