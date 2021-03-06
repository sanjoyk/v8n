# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/)
and this project adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Changed

- Rename `ValidationException` to `ValidationError`

## [1.2.0] - 2018-07-31

### Added

- Rule `passesAnyOf()` to perform branching validation.
- Rule `optional()` for validation of optional values.

### Changed

- Rule `number()` now supports a flag to make it return `false` for infinite numbers ([#76](https://github.com/imbrn/v8n/issues/76))

### Fixed

- `testAsync()` nesting causes for failed validation.

### Deprecated

- From **v2.0.0**: Rule `number()` will return `false` for infinite values by default

## [1.1.2] - 2018-07-26

### Fixed

- Issue with `schema()` not validating at deeper levels properly.

## [1.1.0] - 2018-07-25

### Added

- Ability to receive all validation errors for a value with `testAll()`.
- Ability to create and test asynchronous rules with `testAsync()`.
- Rule `object()` to check whether a value is an object.
- Rule `schema()` to validate the schema of an object.
- Modifier `some` to verify that at least one value in an array passes a rule.
- Modifier `every` to verify that all values in an array pass a rule.

### Changed

- Made `ValidationException` inherit from JavaScript's built-in `Error`.
- Rewrote documentation and moved it from the README to a website using VuePress.
- Made the validation object immutable.

### Fixed

- Build process now properly transpiles modules from ES6 to ES5. ([#44](https://github.com/imbrn/v8n/issues/44))

[unreleased]: https://github.com/imbrn/v8n/compare/v1.2.0...HEAD
[1.2.0]: https://github.com/imbrn/v8n/compare/v1.1.2...v1.2.0
[1.1.2]: https://github.com/imbrn/v8n/compare/v1.1.1...v1.1.2
[1.1.0]: https://github.com/imbrn/v8n/compare/v0.0.1...v1.1.0
