# Shared ESLint and Prettier configuration

This [ESLint](https://eslint.org/) configuration deactivates all formatting rules of ESLint and makes sure that [Prettier](https://prettier.io/) is used for code beautifying. If you want to find out more about this approach, feel free to read my articles on this topic:

- [Efficient Code Analyzing and Formatting (for Vue.js) with ESLint and Prettier](https://doppelmutzi.github.io/efficient-eslint-prettier-vue-workflow/)
- [Efficient Code Analyzing and Formatting (for React) with ESLint, Prettier and VSCode – 2020 Edition](https://doppelmutzi.github.io/react-eslint-prettier-vscode-2020/)
- [Kick-Starting a Sophisticated ESLint and Prettier Workflow with Vue CLI 3 in a few Minutes](https://doppelmutzi.github.io/vuecli-eslint-prettier/)

## Integrate into new project

1. Install this package as devDependency

```sh
# with Yarn
$ yarn add -D @doppelmutzi/eslint-config

# with npm
$ npm i -D @doppelmutzi/eslint-config

# with pnpm
$ pnpm add -D @doppelmutzi/eslint-config
```

2. Install peer dependencies of this package in your project as devDependencies

Therefore, you can make use of the tool [install-peerdeps](https://github.com/nathanhleung/install-peerdeps):

```sh
# with Yarn
$ yarn dlx install-peerdeps --dev @doppelmutzi/eslint-config

# with npm
$ npx install-peerdeps --dev @doppelmutzi/eslint-config

#with pnpm
$ pnpm dlx install-peerdeps --dev @doppelmutzi/eslint-config
```

Instead, you can do this manually my adding all entries part of the `peerDependencies` property (see `package.json`).

3. Use ESLint config in your project

Create a `.eslintrc.js` file in project root with the following content:

```js
module.exports = {
  extends: ["@doppelmutzi/eslint-config"],
};
```