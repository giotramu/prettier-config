# Prettier Config

[Prettier][prettier-url] is an awesome tool and it's focused on doing what it does best, making your code pretty! :sparkles:

That means there's no much effort going into adding support for configuration options, so this project adds them.

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
npx prettier -w -u .
```

## Config

Check the [`.prettierrc.json`](./.prettierrc.json) file if you want to inspect the configuration.

## License

[MIT License](./LICENSE)

<!---
  L I N K S
-->

[prettier-url]: https://prettier.io/
[prettier-doc-url]: https://prettier.io/docs/en/configuration.html
