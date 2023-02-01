<!--

@license Apache-2.0

Copyright (c) 2018 The Stdlib Authors.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

-->

# reBasenamePosix

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> [Regular expression][regexp] to capture the last part of a [POSIX][posix] path.

<section class="installation">

## Installation

```bash
npm install @stdlib/regexp-basename-posix
```

Alternatively,

-   To load the package in a website via a `script` tag without installation and bundlers, use the [ES Module][es-module] available on the [`esm` branch][esm-url].
-   If you are using Deno, visit the [`deno` branch][deno-url].
-   For use in Observable, or in browser/node environments, use the [Universal Module Definition (UMD)][umd] build available on the [`umd` branch][umd-url].

The [branches.md][branches-url] file summarizes the available branches and displays a diagram illustrating their relationships.

</section>

<section class="usage">

## Usage

```javascript
var reBasenamePosix = require( '@stdlib/regexp-basename-posix' );
```

#### reBasenamePosix()

Returns a [regular expression][regexp] to capture the last part of a [POSIX][posix] path. 

```javascript
var RE_BASENAME_POSIX = reBasenamePosix();
var base = RE_BASENAME_POSIX.exec( 'foo/bar/index.js' )[ 1 ];
// returns 'index.js'
```

#### reBasenamePosix.REGEXP

[Regular expression][regexp] to capture the last part of a [POSIX][posix] path. 

```javascript
var base = reBasenamePosix.REGEXP.exec( 'foo/bar/index.js' )[ 1 ];
// returns 'index.js'
```

</section>

<!-- /.usage -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```javascript
var reBasenamePosix = require( '@stdlib/regexp-basename-posix' );

var RE_BASENAME_POSIX = reBasenamePosix();
var base = RE_BASENAME_POSIX.exec( 'index.js' )[ 1 ];
// returns 'index.js'

base = RE_BASENAME_POSIX.exec( '/foo/bar/home.html' )[ 1 ];
// returns 'home.html'

base = RE_BASENAME_POSIX.exec( 'foo/file.pdf' )[ 1 ];
// returns 'file.pdf'

base = RE_BASENAME_POSIX.exec( 'beep.' )[ 1 ];
// returns 'beep.'

base = RE_BASENAME_POSIX.exec( '' )[ 1 ];
// returns ''

base = RE_BASENAME_POSIX.exec( '/foo/bar/file' )[ 1 ];
// returns 'file'

base = RE_BASENAME_POSIX.exec( '/foo/bar/.gitignore' )[ 1 ];
// returns '.gitignore'
```

</section>

<!-- /.examples -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

* * *

## See Also

-   <span class="package-name">[`@stdlib/regexp/basename`][@stdlib/regexp/basename]</span><span class="delimiter">: </span><span class="description">return a regular expression to capture the last part of a path.</span>
-   <span class="package-name">[`@stdlib/regexp/basename-windows`][@stdlib/regexp/basename-windows]</span><span class="delimiter">: </span><span class="description">return a regular expression to capture the last part of a Windows path.</span>

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library for JavaScript and Node.js, with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2023. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/regexp-basename-posix.svg
[npm-url]: https://npmjs.org/package/@stdlib/regexp-basename-posix

[test-image]: https://github.com/stdlib-js/regexp-basename-posix/actions/workflows/test.yml/badge.svg?branch=main
[test-url]: https://github.com/stdlib-js/regexp-basename-posix/actions/workflows/test.yml?query=branch:main

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/regexp-basename-posix/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/regexp-basename-posix?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/regexp-basename-posix.svg
[dependencies-url]: https://david-dm.org/stdlib-js/regexp-basename-posix/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://gitter.im/stdlib-js/stdlib/

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/regexp-basename-posix/tree/deno
[umd-url]: https://github.com/stdlib-js/regexp-basename-posix/tree/umd
[esm-url]: https://github.com/stdlib-js/regexp-basename-posix/tree/esm
[branches-url]: https://github.com/stdlib-js/regexp-basename-posix/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/regexp-basename-posix/main/LICENSE

[regexp]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions

[posix]: https://en.wikipedia.org/wiki/POSIX

<!-- <related-links> -->

[@stdlib/regexp/basename]: https://github.com/stdlib-js/regexp-basename

[@stdlib/regexp/basename-windows]: https://github.com/stdlib-js/regexp-basename-windows

<!-- </related-links> -->

</section>

<!-- /.links -->
