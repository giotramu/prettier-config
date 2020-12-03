# Prettier Config

[Prettier][prettier-url] is an awesome tool and it's focused on doing what it does best: handle the code styles. :sparkles: I bundled my configuration to share it between different projects.

[![NPM][npm-version-img]][npm-url]
[![NPM][npm-download-img]][npm-url]

- [Prettier Config](#prettier-config)
  - [Getting started](#getting-started)
  - [Config](#config)
  - [License](#license)

## Getting started

Install Prettier and the related configuration as a `devDependencies`:

```sh
npm install --save-dev prettier @giotramu/prettier-config
```

Reference it in your `package.json`:

```json
{
  "name": "my-cool-library",
  "version": "1.0.0",
  "prettier": "@giotramu/prettier-config"
}
```

If you don’t want to use `package.json`, you can use any of the [supported extensions][prettier-doc-url] to export a string, e.g. .prettierrc.json:

```json
"@giotramu/prettier-config"
```

> Note: This method does not offer a way to extend the configuration to overwrite some properties from the shared configuration. If you need to do that, import the file in a .prettierrc.js file and export the modifications, e.g:

```js
module.exports = {
  ...require('@giotramu/prettier-config'),
  semi: false
};
```

To format a file in-place, use --write. (Note: This overwrites your files!)

```sh
npx prettier --write .
```

## Config

Check the [`.prettierrc.json`](./.prettierrc.json) file if you want to inspect the configuration.

## License

[MIT License](./LICENSE)

<!---
  I M A G E S
-->

[npm-download-img]: https://img.shields.io/npm/dm/@giotramu/prettier-config?style=flat-square&colorA=202d3a&colorB=0c57fb
[npm-version-img]: https://img.shields.io/npm/v/@giotramu/prettier-config?style=flat-square&colorA=202d3a&colorB=0c57fb

<!---
  L I N K S
-->

[npm-url]: https://www.npmjs.com/package/@giotramu/prettier-config
[prettier-url]: https://prettier.io/
[prettier-doc-url]: https://prettier.io/docs/en/configuration.html
