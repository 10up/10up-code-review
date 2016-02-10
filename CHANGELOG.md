# Changelog

## [0.2.0] - 2016-02-02

* Include an installation script in `bin/install` to automatically configure PHP_CodeSniffer.
* Automatically run the installation script on Composer install/update.
* Move existing standards into the root of the package.
* Update documentation to remove references to manual installation or the `standards` directory.

## [0.1.1] - 2016-01-29

* Update documentation to reflect correct path to coding standards.
* Remove version number from composer.json, as both [Packagist and Composer can read this from our semantic release tags](https://getcomposer.org/doc/04-schema.md#version):

	> Optional if the package repository can infer the version from somewhere, such as the VCS tag name in the VCS repository. In that case it is also recommended to omit it.


## 0.1.0 - 2016-01-29

* Initial public release and publish to Packagist.


[0.2.0]: https://github.com/10up/10up-coding-standards/compare/v0.1.1...master
[0.1.1]: https://github.com/10up/10up-coding-standards/compare/v0.1.0...v0.1.1