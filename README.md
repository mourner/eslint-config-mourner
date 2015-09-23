## eslint-config-mapbox

A [ESLint](http://eslint.org/) config for Mapbox JavaScript projects.

It is meant to be very strict, enforcing as many rules and conventions as possible,
to keep our code clean, elegant and consistent across projects.
These rules are easy to follow, so this is good for new projects,
while being easy to disable on a case by case basis for existing projects
if you want to enforce and fix them gradually or have justified exceptions.

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

### Automatic fixes

To make things easier, you can run `eslint` with `--fix` option
that automatically fixes all simple errors like indentation and quotes for you.

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
