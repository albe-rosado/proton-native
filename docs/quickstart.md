# Quickstart

## Prerequisites

### Linux

`libgtk-3-dev`

## Install

### Automatic 

``` zsh
# install the cli app
npm install -g create-proton-app
# create your project
create-proton-app my-app
# move to your project directory
cd my-app
# run your app
npm run start
```
You can alternatively use `npx` if you prefer.

### Manual

To install, simply download it from NPM:
`npm i -S proton-native`

If you get an error about Python on Windows, install the build tools:
`npm install --global --production windows-build-tools`

## Setup

Create `.babelrc`:

```
{
    "presets": [
      "env",
      "stage-0",
      "react"
    ]
}
```

And then add the following to your `package.json`:

```
  "scripts": {
    "start": "node_modules/.bin/babel-node index.js"
  }
```

Now you can just run `npm run start` to run your script.

## index.js

A usual example starts with the following, just like any other React Native app. Most props can be set to their defaults and not be mentioned, as shown above. The Window component actually accepts many props, but only 4 have to be specified.

``` javascript
import React, { Component } from 'react'; // import from react

import { render, Window, App } from 'proton-native'; // import the proton-native components

class Example extends Component {
  render() { // all Components must have a render method
    return (
      <App> // you must always include App around everything
        <Window title="Example" height={300} width={300} menuBar={false}>
            // all your other components go here
        </Window>
      </App>
    );
  }
}

render(<Example />); // and finally render your main component
```

Use all your usual state and component workflow.

