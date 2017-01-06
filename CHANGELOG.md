# Changelog

## [Unreleased]

* Added the "10up-Third-Party" standard, a subset of the 10up-Code-Review standard that ignores code issues that _we'd_ never want to put in our code but are pretty common (and relatively harmless) when reviewing third-party code.

## [Unreleased]

* Remove sniffs for "camel cap" class names when reviewing third-party code.


## [0.2.0] - 2016-02-10

* Remove sniffs for function declaration whitespace and WordPress naming conventions from the 10up-Code-Review ruleset.
* Added `10up-code-review-install` installation script to append (rather than overwrite) existing PHP_CodeSniffer configuration ([#3], [#4]).
* Move existing standards into the root of the package ([#2]).
* Update documentation to remove references to manual installation or the `standards` directory ([#3]).


## [0.1.1] - 2016-01-29

* Update documentation to reflect correct path to coding standards.
* Remove version number from composer.json, as both [Packagist and Composer can read this from our semantic release tags](https://getcomposer.org/doc/04-schema.md#version):

	> Optional if the package repository can infer the version from somewhere, such as the VCS tag name in the VCS repository. In that case it is also recommended to omit it.


## 0.1.0 - 2016-01-29

* Initial public release and publish to Packagist.


[Unreleased]: https://github.com/10up/10up-coding-standards/compare/master...develop
[0.2.0]: https://github.com/10up/10up-coding-standards/compare/v0.1.1...v0.2.0
[0.1.1]: https://github.com/10up/10up-coding-standards/compare/v0.1.0...v0.1.1
[#2]: https://github.com/10up/10up-code-review/issues/2
[#3]: https://github.com/10up/10up-code-review/issues/3
[#4]: https://github.com/10up/10up-code-review/issues/4