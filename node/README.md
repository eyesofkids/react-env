# Node

## Install and config package.json

> package.json

type can be "module" or "commonjs"

```json
"engines": {
    "node": ">=8.10.0"
  },
  "type": "module",
```

> install eslint and prettier

```sh
npm i --save-dev prettier eslint-config-prettier eslint-plugin-prettier eslint eslint-plugin-node
```

## ES6 module support

### Node >= v13

either

1. Save the file with .mjs extension
2. Add { "type": "module" } in package.json.


### Node <= v12

Save the file with ES6 modules with .mjs extension and run it like:

```sh
node --experimental-modules my-app.mjs
```
