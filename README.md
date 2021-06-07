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

# Basename

> [Regular expression][regexp] to capture the last part of a [POSIX][posix] path.

<section class="installation">

## Installation

```bash
npm install @stdlib/regexp-basename-posix
```

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


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library for JavaScript and Node.js, with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2021. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/regexp-basename-posix/main/LICENSE

[regexp]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions

[posix]: https://en.wikipedia.org/wiki/POSIX

</section>

<!-- /.links -->
