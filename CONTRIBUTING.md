# Contributing to 10up Code Reviews

If you're contributing to this repository, you likely a) already work for 10up or b) appreciate what we're doing and want to leverage this in your own workflow (btw, [we're hiring](http://10up.com/careers/)). Either way, welcome!

To get started, install the dev dependencies for this project via Composer:

```bash
$ composer install
```

Wow, that was easy! From here, start creating new rulesets based on the [PHP_CodeSniffer annotated ruleset.xml](https://github.com/squizlabs/PHP_CodeSniffer/wiki/Annotated-ruleset.xml).

## Guidelines

1. All new standards should be prefixed with "10up" (or your company/team name, if you've forked this repository). This is to make it clear that they're for internal use, not for the general population to check all of their code against (they should be using the [WordPress Coding Standards](https://github.com/WordPress-Coding-Standards/WordPress-Coding-Standards) for that).
2. Please follow the conventions of the repository: new standards should go in `standards/<10up-My-New-Standard>/ruleset.xml`, where the standard's directory matches the `name` attribute on the `<ruleset />` node and is title-cased. Also, don't forget to add your new standard to the README file!
3. Please start new rulesets by loading the 10up-Base standard, as that standard starts with WordPress-Extra but adds in a series of `<exclude-pattern />` nodes (based on the [10up Engineering Best Practices](https://10up.github.io/Engineering-Best-Practices/structure/)) and handling for some common PHP_CodeSniffer internal warnings.