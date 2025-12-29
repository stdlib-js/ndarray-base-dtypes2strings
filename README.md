<!--

@license Apache-2.0

Copyright (c) 2025 The Stdlib Authors.

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


<details>
  <summary>
    About stdlib...
  </summary>
  <p>We believe in a future in which the web is a preferred environment for numerical computation. To help realize this future, we've built stdlib. stdlib is a standard library, with an emphasis on numerical and scientific computation, written in JavaScript (and C) for execution in browsers and in Node.js.</p>
  <p>The library is fully decomposable, being architected in such a way that you can swap out and mix and match APIs and functionality to cater to your exact preferences and use cases.</p>
  <p>When you use stdlib, you can be absolutely certain that you are using the most thorough, rigorous, well-written, studied, documented, tested, measured, and high-quality code out there.</p>
  <p>To join us in bringing numerical computing to the web, get started by checking us out on <a href="https://github.com/stdlib-js/stdlib">GitHub</a>, and please consider <a href="https://opencollective.com/stdlib">financially supporting stdlib</a>. We greatly appreciate your continued support!</p>
</details>

# dtypes2strings

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Resolve a list of [data type][@stdlib/ndarray/dtypes] strings.

<!-- Section to include introductory text. Make sure to keep an empty line after the intro `section` element and another before the `/section` close. -->

<section class="intro">

</section>

<!-- /.intro -->

<!-- Package usage documentation. -->



<section class="usage">

## Usage

To use in Observable,

```javascript
dtypes2strings = require( 'https://cdn.jsdelivr.net/gh/stdlib-js/ndarray-base-dtypes2strings@umd/browser.js' )
```

To vendor stdlib functionality and avoid installing dependency trees for Node.js, you can use the UMD server build:

```javascript
var dtypes2strings = require( 'path/to/vendor/umd/ndarray-base-dtypes2strings/index.js' )
```

To include the bundle in a webpage,

```html
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/ndarray-base-dtypes2strings@umd/browser.js"></script>
```

If no recognized module system is present, access bundle contents via the global scope:

```html
<script type="text/javascript">
(function () {
    window.dtypes2strings;
})();
</script>
```

#### dtypes2strings( dtypes )

Resolves a list of [data type][@stdlib/ndarray/dtypes] strings.

```javascript
var DataType = require( '@stdlib/ndarray-dtype-ctor' );

var out = dtypes2strings( [ new DataType( 'float32' ), new DataType( 'float64' ) ] );
// returns [...]
```

The function accepts the following arguments:

-   **dtypes**: an array of [data types][@stdlib/ndarray/dtypes].

If the function is unable to resolve a data type string for a provided [data type][@stdlib/ndarray/dtypes], the corresponding element in the returned array will be `null`.

```javascript
var out = dtypes2strings( [ 'foo', 'bar' ] );
// returns [ null, null ]
```

</section>

<!-- /.usage -->

<!-- Package usage notes. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="notes">

</section>

<!-- /.notes -->

<!-- Package usage examples. -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```html
<!DOCTYPE html>
<html lang="en">
<body>
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/ndarray-dtypes@umd/browser.js"></script>
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/console-log-each@umd/browser.js"></script>
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/ndarray-base-dtypes2strings@umd/browser.js"></script>
<script type="text/javascript">
(function () {

// Get the list of supported data types:
var dt = dtypes();

// Resolve strings:
var strs = dtypes2strings( dt );

// Print the results:
logEach( '%s => %s', dt, strs );

})();
</script>
</body>
</html>
```

</section>

<!-- /.examples -->

<!-- Section to include cited references. If references are included, add a horizontal rule *before* the section. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="references">

</section>

<!-- /.references -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

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

Copyright &copy; 2016-2025. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/ndarray-base-dtypes2strings.svg
[npm-url]: https://npmjs.org/package/@stdlib/ndarray-base-dtypes2strings

[test-image]: https://github.com/stdlib-js/ndarray-base-dtypes2strings/actions/workflows/test.yml/badge.svg?branch=main
[test-url]: https://github.com/stdlib-js/ndarray-base-dtypes2strings/actions/workflows/test.yml?query=branch:main

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/ndarray-base-dtypes2strings/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/ndarray-base-dtypes2strings?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/ndarray-base-dtypes2strings.svg
[dependencies-url]: https://david-dm.org/stdlib-js/ndarray-base-dtypes2strings/main

-->

[chat-image]: https://img.shields.io/badge/zulip-join_chat-brightgreen.svg
[chat-url]: https://stdlib.zulipchat.com

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/ndarray-base-dtypes2strings/tree/deno
[deno-readme]: https://github.com/stdlib-js/ndarray-base-dtypes2strings/blob/deno/README.md
[umd-url]: https://github.com/stdlib-js/ndarray-base-dtypes2strings/tree/umd
[umd-readme]: https://github.com/stdlib-js/ndarray-base-dtypes2strings/blob/umd/README.md
[esm-url]: https://github.com/stdlib-js/ndarray-base-dtypes2strings/tree/esm
[esm-readme]: https://github.com/stdlib-js/ndarray-base-dtypes2strings/blob/esm/README.md
[branches-url]: https://github.com/stdlib-js/ndarray-base-dtypes2strings/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/ndarray-base-dtypes2strings/main/LICENSE

[@stdlib/ndarray/dtypes]: https://github.com/stdlib-js/ndarray-dtypes/tree/umd

</section>

<!-- /.links -->
