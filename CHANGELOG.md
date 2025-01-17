# Change Log

All notable changes to the "jsdoc-generator" extension will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

Nothing new

## [1.3.0] - 2023/07/21

### Added

- New setting option to create custom tags.

## [1.2.0] - 2023/02/26

### Added

- Setting to toggle whether to include types (defaults to `true`).
- Support for JavaScript and JavaScript React.

### Changed

- Template tags now correctly only show the name of the type parameter.

### Fixed

- Fixed [#5](https://github.com/Nyphet/jsdoc-generator/issues/5).
- Fixed unnecessary brackets around union or intersection types.  
  For example, `Type<T & U>` before became `(Type<T & U>)`, now it correctly stays as `Type<T & U>`.

## [1.1.1] - 2022/04/09

### Added

- Setting to toggle whether to include export tag
- Setting to toggle whether to include async tag

## [1.1.0] - 2021/12/03

### Added

- Support for TypeScript React.

### Changed

- A few minor project configuration settings with consequent fixes.

## [1.0.0] - 2021/07/20

### Added

- 3 commands declarations.
- Extension configurations.
- Bundling.
- [README] file.
- JSDoc single node generation (1st command).
- JSDoc single node generation with completion.
- JSDoc single file generation (2nd command).
- Type inference to generate more precise JSDoc.
- Few basic unit tests.
- This [CHANGELOG] file.

[unreleased]: https://github.com/Nyphet/jsdoc-generator
[1.3.0]: https://github.com/Nyphet/jsdoc-generator/releases/tag/v1.3.0
[1.2.0]: https://github.com/Nyphet/jsdoc-generator/releases/tag/v1.2.0
[1.1.1]: https://github.com/Nyphet/jsdoc-generator/releases/tag/v1.1.1
[1.1.0]: https://github.com/Nyphet/jsdoc-generator/releases/tag/v1.1.0
[1.0.0]: https://github.com/Nyphet/jsdoc-generator/releases/tag/v1.0.0
[readme]: https://github.com/Nyphet/jsdoc-generator
[changelog]: https://github.com/Nyphet/jsdoc-generator/blob/main/CHANGELOG.md
