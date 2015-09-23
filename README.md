## eslint-config-mapbox

A [ESLint](http://eslint.org/) config for Mapbox JavaScript projects.

### Install

To use it in your project, run:

```bash
npm install --save-dev eslint eslint-config-mapbox
```

Then add a following `.eslintrc` file in the repo root:

```json
{
  "extends": "eslint-config-mapbox"
}
```

Finally, add `eslint` to your `npm test` script in `package.json`:

```json
"scripts": {
  "test": "eslint index.js && tap test/test*.js",
}
```

Now run `npm test` and enjoy thousands of errors! :)

### Fix errors

To make things easier, you can run `eslint` with `--fix` option
that automatically fixes a lot of errors like indentation and quotes for you.

### Overrides

Some of the rules may be too strict for your project,
but you can easily override any rules or options like this:

```json
{
  "extends": "eslint-config-mapbox",
  "rules": {
    "yoda": 0,
    "indent": [2, 2]
  },
  "env": {
    "mocha": true
  }
}
```
