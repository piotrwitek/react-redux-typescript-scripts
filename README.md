<div align="center">
<h1>react-redux-typescript-scripts 🛠</h1>

<p>Shared dev-tools configuration files based on <a href="https://github.com/piotrwitek/react-redux-typescript-guide">react-redux-typescript-guide</a></p>
</div>

---

> For now you can find `eslint`, `tslint` and `tsconfig` configurations, but I'm willing to add more tools and scripts in the future e.g. `jest`, `babel`, npm scripts etc.

> I'm open to suggestion on improvements like adding or changing default rules so please feel free to open an issue.

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
    - [.eslintrc](#eslintrc)
    - [create-react-app](#create-react-app)
- [LICENSE](#license)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

---

## Installation

1. This package is distributed via npm and should be installed as `devDependencies`:

```
npm i -D react-redux-typescript-scripts
```

2. You should also install optional dependencies depending on 

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
> WARNING: When using this config you need to install `tslint` as dependency in your project.

There are few configs available (you can use one or all by declaring an array in `extends` config property):
  - `react-redux-typescript-scripts/tslint.json` - mandatory base config - based on recommended rules.
  - `react-redux-typescript-scripts/tslint-react.json`- include react rules - based on `tslint-react`.

#### tslint.json
```ts
{
  "extends": [
    "react-redux-typescript-scripts/tslint.json", 
    "react-redux-typescript-scripts/tslint-react.json" // optional
  ],
  "rules": {
    // you can further customize options here
  }
}
```

### ESLint
> WARNING: When using this config you need to install `eslint` as dependency in your project.

There are few configs available (you can use one or all by declaring an array in `extends` config property):
  - `./node_modules/react-redux-typescript-scripts/eslint.json` - mandatory base config - based on recommended rules.
  - `./node_modules/react-redux-typescript-scripts/eslint-prettier.json`- disable eslint formatting related rules conflicting with prettier - based on `eslint-config-prettier` _(**WARNING:** Should be the last one in `extends` array)_.

#### .eslintrc
```ts
{
  "extends": [
    "./node_modules/react-redux-typescript-scripts/eslint.js",
    "./node_modules/react-redux-typescript-scripts/eslint-prettier.js" // optional
  ],
  "rules": {
    // you can further customize options here
  }
}
```

#### create-react-app
To fully integrate `@typescript-eslint` with your `create-react-app` add below snippet to your `.eslintrc` or `package.json` under the `eslintConfig` key:
```ts
{
  "extends": [
    "react-app",
    "./node_modules/react-redux-typescript-scripts/eslint.js",
    "./node_modules/react-redux-typescript-scripts/eslint-prettier.js" // optional
  ],
}
```

## LICENSE

[MIT](./LICENSE)
