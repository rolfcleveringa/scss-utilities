# scss-utilities

[![NPM](https://img.shields.io/npm/v/scss-utilities.svg?style=flat-square)](https://www.npmjs.com/package/scss-utilities)
[![License: MIT](https://img.shields.io/npm/l/scss-utilities?style=flat-square)](https://github.com/rolfcleveringa/scss-utilities/blob/main/LICENSE)

A collection of [Sass](https://sass-lang.com/) functions and mixins.

> Please don't use this package yet. For now it's just to test some things with npm packages.

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

_Note: please make sure you add the correct path. It may be you have your sass file in a subdirectory._

## Usage

scss-utilities is a collection of usefull mixins and functions. You can use them directly in your own code.

```scss
@use "scss-utilities" as *;

ul {
    @include list-unstyled();
}
```

In order to prevent naming conflicts, you can also prefix the package, like so:


```scss
@use "scss-utilities" as su;

ul {
    @include su.list-unstyled();
}
```

## Support

- Create a [GitHub issue](https://github.com/rolfcleveringa/scss-utilities/issues/new/choose) for bug reports and feature requests.

## License

This project is licensed under the MIT License. See the [LICENSE](https://github.com/rolfcleveringa/scss-utilities/blob/main/LICENSE) for details.
