<div align="center">
<h1>react-redux-typescript-scripts 🛠</h1>

<p>Shared dev-tools configuration files based on <a href="https://github.com/piotrwitek/react-redux-typescript-guide">react-redux-typescript-guide</a></p>
</div>

---

> For now you can find `tslint` and `tsconfig` configurations, but I'm willing to add more tools and scripts in the future e.g. `jest`, `babel`, `eslint`, npm scripts etc.

---

## Table of Contents

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->


- [Installation](#installation)
- [Usage](#usage)
  - [tsconfig.json](#tsconfigjson)
  - [TSLint](#tslint)
    - [tslint.json](#tslintjson)
  - [ESLint](#eslint)
    - [`create-react-app`](#create-react-app)
- [LICENSE](#license)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

---

## Installation

This module is distributed via npm package and
should be installed as one of your project's `devDependencies`:

```
npm i -D react-redux-typescript-scripts
```

## Usage

You can find usage instructions for each tool in it's onw section below.

### tsconfig.json
```ts
{
  "include": ["./src"],
  "extends": "./node_modules/react-redux-typescript-scripts/tsconfig.json",
  "compilerOptions": {
    // you can further customize options here
  }
}
```

### TSLint
Following configs are available to extend (you can use one or all by declaring an array in `extends` config property):
  - `react-redux-typescript-scripts/tslint.json` - best default config - based on recommended tslint built-in config.
  - `react-redux-typescript-scripts/tslint-react.json`- for react projects - based on `tslint-react`.

#### tslint.json
```ts
{
  "extends": [
    "react-redux-typescript-scripts/tslint.json", 
    "react-redux-typescript-scripts/tslint-react.json"
  ],
  "rules": {
    // you can further customize options here
  }
}
```

### ESLint

#### .eslintrc
```ts
{
  "extends": [
    "./node_modules/react-redux-typescript-scripts/eslint.js"
  ],
  "rules": {
    // you can further customize options here
  }
}
```

#### create-react-app
This single change will fully integrate `@typescript-eslint` config with your `create-react-app`:
```ts
{
  "eslintConfig": {
    "extends": [
      "react-app",
      "./node_modules/react-redux-typescript-scripts/eslint.js"
    ],
  }
}
```

## LICENSE

[MIT](./LICENSE)
