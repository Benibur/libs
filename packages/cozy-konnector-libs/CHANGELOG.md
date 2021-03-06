# Changelog

## [Unreleased]

### Changed
- none yet

### Fixed
- none yet

### Added
- none yet

## cozy-jobs-cli@1.0.17, cozy-konnector-libs@4.1.7, cozy-logger@1.1.4 (2018-04-17)

#### :bug: Bug Fix
* `cozy-logger`
  * [#202](https://github.com/konnectors/libs/pull/202) fix: cannot assign from error to object. ([@ptbrowne](https://github.com/ptbrowne))

#### Committers: 1
- Patrick Browne ([ptbrowne](https://github.com/ptbrowne))

## cozy-konnector-libs@4.1.6 (2018-04-17)

#### :rocket: Enhancement
* `cozy-konnector-libs`
  * [#200](https://github.com/konnectors/libs/pull/200) fix: formatting of error is done in cozy-logger. ([@ptbrowne](https://github.com/ptbrowne))

## cozy-konnector-libs@4.1.2 (2018-04-10)

#### :bug: Bug Fix
* `cozy-konnector-libs`
  * [#180](https://github.com/konnectors/libs/pull/180) 🐝 fix: use target node 8 to remove the need for regeneratorRuntime. ([@ptbrowne](https://github.com/ptbrowne))


## [4.1.0] (2018-04-09)

#### :rocket: Enhancement
* Other
  * [#178](https://github.com/konnectors/libs/pull/178) ✨ feat: add lerna changelog. ([@ptbrowne](https://github.com/ptbrowne))
* `cozy-logger`
  * [#177](https://github.com/konnectors/libs/pull/177) feat: if message is an object, its properties are assigned to the log. ([@ptbrowne](https://github.com/ptbrowne))

#### :bug: Bug Fix
* `cozy-jobs-cli`
  * [#172](https://github.com/konnectors/libs/pull/172) fix: yarn dev now works without defining the file source. ([@doubleface](https://github.com/doubleface))

## [4.0.0] - 2018-04-06

### Changed

- `cozy-konnector-libs` : Changed linking mechanism to in-memory
- `cozy-konnector-libs`: `updateOrCreate` is no longer deprecated.
- `cozy-konnector-libs`: transpiled sources are shipped on npm

## [3.8.1] - 2018-03-29

### Fixed

- `cozy-konnector-libs` No longer has bin in package.json. Moved to cozy-konnector-libs.

## [3.8.0] - 2018-03-27

### Added
- `cozy-konnector-libs`: `signin` helper. Should make sign in process to websites easier [#138](https://github.com/cozy/cozy-konnector-libs/pull/138). Big thank you to @carrieje :+1: !
- `cozy-konnector-libs`: banking operation categorized as "health insurance" can be considered for linking with an health bill if its amount is greater than 0 (previously only operation categorized as "health expenses" were considered for linking)
- `cozy-konnector-libs`: bill matching logs are tinier
- `cozy-jobs-cli`: allow to parse an HTML file from the shell

## [3.7.0] - 2018-03-13

- Update cozy-client-js
- Use lerna

## [3.6.0] - 2018-03-12

### Added

- `scrape` function.

## [3.5.3] - 2018-03-08

### Added

- Document class
- saveFiles handles filestreams (Thanks [Jérémie](https://github.com/laedit) !)
- `fetch` function return value is checked to be a Promise

## [3.5.2] - 2018-02-28

### Fixed
- Banking operations cannot have reimbursements total amount be higher than their amount

## [3.5.1] - 2018-02-21

### Fixed

- Default log level is not "debug" instead of "info". The stack filters out
debug logs but "info" are kept.

### Added

- `shouldSave` and `shouldUpdate` functions  can be passed to hydrateAndFilter. It allows for finer grained control over what is saved/updated.

### Deprecated

- `updateOrCreate` is now deprecated. Prefer to use `shouldSave`/`shouldUpdate`.

## [3.3.0] - 2018-01-23

### Added
- Automatic exception handling via Sentry if `process.env.SENTRY_DSN` is set

### Fixed
- Correct status codes are used when exiting from an error
- Yarn dev

## [3.2.4] - 2018-01-23
### Changed
- Fixed linking of health bills to their credit operation when no debit operation found

## [3.2.4] - 2018-01-22
### Changed
- Fixed linking of health bills to operations
- More details when an error message is caught by the BaseKonnector

## [3.2.3] - 2018-01-19
### Changed
- Now by default, mathing bill operation check the range date with - 15 days + 29 days


## [3.2.1] - 2018-01-18
### Fixed
- Remove spread es6 syntax


## [3.2.0] - 2018-01-18
### Changed
- Refactoring of bills and transactions association

### Fixed
- operation.reimbursements can't have same reimbursement


## [3.1.6] - 2018-01-17
### Fixed
- Linking with bank operations also works on first run


## [3.1.5] - 2018-01-10
### Fixed
- Linking with bank operations now works even if the bill has already been fetched

## Details

The format is based on [Keep a Changelog](http://keepachangelog.com/)
and this project adheres to [Semantic Versioning](http://semver.org/).

[Unreleased]: https://github.com/cozy/cozy-konnector-libs/compare/cozy-konnector-libs@4.1.0...HEAD
[4.1.0]: https://github.com/cozy/cozy-konnector-libs/compare/cozy-konnector-libs@4.0.0...4.1.0
[4.0.0]: https://github.com/cozy/cozy-konnector-libs/compare/cozy-konnector-libs@3.8.2...cozy-konnector-libs@4.0.0
[3.8.2]: https://github.com/cozy/cozy-konnector-libs/compare/v3.8.1...v3.8.2
[3.8.1]: https://github.com/cozy/cozy-konnector-libs/compare/v3.8.0...v3.8.1
[3.8.0]: https://github.com/cozy/cozy-konnector-libs/compare/v3.7.0...v3.8.0
[3.7.0]: https://github.com/cozy/cozy-konnector-libs/compare/v3.6.0...v3.7.0
[3.6.0]: https://github.com/cozy/cozy-konnector-libs/compare/v3.5.3...v3.6.0
[3.5.3]: https://github.com/cozy/cozy-konnector-libs/compare/v3.5.2...v3.5.3
[3.5.2]: https://github.com/cozy/cozy-konnector-libs/compare/v3.5.1...v3.5.2
[3.5.1]: https://github.com/cozy/cozy-konnector-libs/compare/v3.3.0...v3.5.1
[3.3.0]: https://github.com/cozy/cozy-konnector-libs/compare/v3.2.5...v3.3.0
[3.2.5]: https://github.com/cozy/cozy-konnector-libs/compare/v3.2.4...v3.2.5
[3.2.4]: https://github.com/cozy/cozy-konnector-libs/compare/v3.2.3...v3.2.4
[3.2.3]: https://github.com/cozy/cozy-konnector-libs/compare/v3.2.2...v3.2.3
[3.2.2]: https://github.com/cozy/cozy-konnector-libs/compare/v3.2.1...v3.2.2
[3.2.1]: https://github.com/cozy/cozy-konnector-libs/compare/v3.2.0...v3.2.1
[3.2.0]: https://github.com/cozy/cozy-konnector-libs/compare/v3.1.6...v3.2.0
[3.1.6]: https://github.com/cozy/cozy-konnector-libs/compare/176b49b...v3.1.6
[3.1.5]: https://github.com/cozy/cozy-konnector-libs/compare/8b00eda...176b49b
