# 10up Code Review

[![Packagist](https://img.shields.io/packagist/v/10up/10up-code-review.svg)](https://packagist.org/packages/10up/10up-code-review)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](https://github.com/10up/10up-code-review#license)

This package is a collection of standards for [PHP_CodeSniffer](https://github.com/squizlabs/PHP_CodeSniffer) to aid engineers at [10up](http://10up.com) when preparing for or performing code reviews.

**This does not replace an actual code review**, but rather helps reviewers and engineers alike catch the low-hanging fruit so that they can focus on the hard stuff!

## Installation

The easiest way to install the package is globally, using Composer:

```
$ composer global require 10up/10up-code-review
```

Once installed, you'll want to set PHP_CodeSniffer's path to the 10up rulesets (which also include the various [WordPress Coding Standards rulesets](https://github.com/WordPress-Coding-Standards/WordPress-Coding-Standards)):

```bash
$ phpcs --config-set installed_paths /path/to/10up-code-review/standards
```

You can also install the package on a per-project basis:

```bash
$ composer require --dev 10up/10up-code-review
$ vendor/bin/phpcs --config-set installed_paths ../../10up/10up-code-review/standards
```

## Usage

From the command line, run the following:

```bash
$ phpcs --standard=10up-Code-Review path/to/your/project
```

As this is just a collection of custom rulesets, the [usual PHP_CodeSniffer](https://github.com/squizlabs/PHP_CodeSniffer/wiki/Usage) commands still apply.


## Standards

This package contains the following rulesets for PHP_CodeSniffer:

### 10up-Base

> A base ruleset that all other 10up rulesets should extend.

This ruleset sets some default `<ignore-pattern />` paths based on those dictated by [the 10up Engineering Best Practices](https://10up.github.io/Engineering-Best-Practices/structure/) and [generator-wp-make](https://github.com/10up/generator-wp-make).

### 10up-Code-Review

> Apply the WordPress coding standards, focusing on things like sanitization, late-escaping, etc. but not making noise about documentation, whitespace, etc.

This will likely be the default coding standard that you'll use when performing code reviews; it's based on the WordPress-Extra standard but removes complaints about whitespace and general formatting, letting you focus on the important issues like performance, sanitization, late-escaping, etc.


## License

The MIT License (MIT)
Copyright (c) 2016 10up, LLC

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.