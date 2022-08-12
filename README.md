# scss-utilities

[![NPM](https://img.shields.io/npm/v/sass-utilities.svg?style=flat-square)](https://www.npmjs.com/package/scss-utilities)
[![License: MIT](https://badgen.net/github/license/micromatch/micromatch)](https://github.com/WOTstorm/scss-utilities/blob/main/LICENSE)

A collection of [Sass](https://sass-lang.com/) functions and mixins.

## Installation

**NPM**

In the command line with NPM:

```shell
npm install scss-utilities --save-dev
```

**Sass**

Import the Sass package at the top of your main Sass file:

```scss
// Import the package in
@use "scss-utilities" as *;
```

Depending on your setup, you may need to include the full path name:

```scss
@use "../node_modules/scss-utilities/scss-utilities" as *;
```

## Usage

scss-utilities is a collection of usefull mixins and functions. You can use them directly in your own code.

```scss
@use "scss-utilities" as su;

ul {
    @include su.list-unstyled();
}
```

## Support

- Create a [GitHub issue](https://github.com/WOTstorm/scss-utilities/issues/new/choose) for bug reports and feature requests.

## License

This project is licensed under the MIT License. See the [LICENSE](https://github.com/WOTstorm/scss-utilities/blob/main/LICENSE) for details.
