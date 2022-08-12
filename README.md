# sass-utilities

[![NPM](https://img.shields.io/npm/v/sass-utilities.svg?style=flat-square)](https://www.npmjs.com/package/scss-utilities)
[![License: MIT](https://badgen.net/github/license/micromatch/micromatch)](https://github.com/WOTstorm/scss-utilities/blob/master/LICENSE)

A collection of [Sass](https://sass-lang.com/) classes, functions, mixins, and other utilities.

- [Documentation](https://jhildenbiddle.github.io/sass-utilities/) (via [SassDoc](http://sassdoc.com/))

## Installation

**NPM**

```shell
npm install sass-utilities
```

```scss
// All utilities
@use "sass-utilities";

// All functions
@use "sass-utilities/functions";

// All mixins
@use "sass-utilities/mixins";

// Single function
@use "sass-utilities/functions/_file-name";

// Single mixin
@use "sass-utilities/mixins/_file-name";
```

## Install

In the command line with NPM: 
```js
npm install sass-utilizer --save-dev
```

Import into your directory:
```scss
@use 'sass-utilizer' as *;
```

Depending on your setup, you may need to include the full path name: 
```scss
@use '../node_modules/sass-utilizer/utilizer' as *;
```
## Usage

```scss
// All utilities (installed via npm)
@use "sass-utilities" as su;

div {
    @include su.triangle(right, 16px);
}
```

## Usage

At its core, Sass Utilizer is essentially a mixin that will consume basic utilities and generate utilities of exponential complexity as a result of how you've configured them.

Here's an example of setting up Utilizer with a basic margin utility:

```scss
@use 'sass-utilizer';

$utilities: (
    m: (
        styles: (
            margin: 1rem
        ),
        directions: true,
        increments: true,
        negatives: true,
        breakpoints: true,
        pseudos: (hover, focus)
    )
);

$bpConfig: (
    breakpoints: (
        sm: 568px,
        md: 780px,
        lg: 1200px,
    ),
    paradigm: min-width
);

@include sass-utilizer.render($utilities, $bpConfig);
```

To outline the above:

* Utilizer accepts two arguments, a map of your utilities and the configuration for your breakpoints
* The label of the utility specified in `$utilities`, in this case `m`, is what Utilizer will use for the class name later on
* Style rules go in the nested `styles` map
* All properties, excluding `styles`, relate to configuration for generating utilities
* The second argument will consume any breakpoints listed in your breakpoint config variable and specify which breakpoint utility to generate with what rules
* The paradigm property in your breakpoint config will specify whether or not you want your utilities to be mobile-first or desktop-first.


## Contact & Support

- Create a [GitHub issue](https://github.com/jhildenbiddle/sass-utilities/issues) for bug reports, feature requests, or questions
- Follow [@jhildenbiddle](https://twitter.com/jhildenbiddle) for announcements
- Add a ⭐️ [star on GitHub](https://github.com/jhildenbiddle/sass-utilities) or 🐦 [tweet](https://twitter.com/intent/tweet?url=https%3A%2F%2Fgithub.com%2Fjhildenbiddle%2Fsass-utilities&hashtags=css,sass,scss,developers,frontend) to support the project!

## License

This project is licensed under the MIT License. See the [LICENSE](https://github.com/jhildenbiddle/sass-utilities/blob/master/LICENSE) for details.

Copyright (c) John Hildenbiddle ([@jhildenbiddle](https://twitter.com/jhildenbiddle))
