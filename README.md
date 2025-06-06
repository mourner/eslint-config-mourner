## eslint-config-mourner

A great [ESLint](http://eslint.org/) config with sensible defaults
that I use in [all my JavaScript projects](https://github.com/mourner/projects).

It is meant to be _strict_, enforcing as many useful rules and conventions as possible
to keep the code clean, elegant and consistent across projects.

The rules are easy to follow, so this is a good starting place for new projects,
while being easy to disable on a case by case basis for existing projects
if you want to enforce and fix them gradually or have justified exceptions.

### Install

To use it in your project, run:

```bash
npm init @eslint/config@latest -- --config eslint-config-mourner
```

Which will add a `eslint.config.[js|mjs]` file in the repo root.

Finally, add `eslint` to a `package.json` script:

```json
"scripts": {
  "lint": "eslint index.js test/test*.js",
  "pretest": "npm run lint"
}
```

Now run `npm run lint` and enjoy all the errors! :)

### Automatic fixes

To make things easier, you can run `eslint` with `--fix` option
that automatically fixes all simple errors like indentation and quotes for you.

