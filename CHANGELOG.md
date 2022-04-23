# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog][keepachangelog] and this project
adheres to [Semantic Versioning][semver].

## [Unreleased]

## [2.2.1] - 2022-04-23
### Fixed
- Fix action version references

## [2.2.0] - 2022-02-28
### Added
- Add Drupal extension continuous integration reusable workflow

## [2.1.6] - 2022-02-21
### Fixed
- Fix config updates always run with dev modules

## [2.1.5] - 2022-01-06
### Fixed
- Fix config file deletions not committed

## [2.1.4] - 2022-01-06
### Fixed
- Fix error attempting to commit untracked config

## [2.1.3] - 2022-01-06
### Fixed
- Ensure final newline exists for exported config

## [2.1.2] - 2021-12-24
### Changed
- Optimize PR HEAD commit fetch for human commits only

### Fixed
- Fix `[skip *]` tags not working in PRs

## [2.1.1] - 2021-12-17
### Changed
- Run config updates on dependabot actions only

## [2.1.0] - 2021-12-17
### Added
- Add config updating for dependabot PRs

## [2.0.0] - 2021-12-11
### Changed
- Parse WordPress theme deployment target info from wp-cli @live alias

### Removed
- Remove WordPress theme CI/CD `deploy_target` and `deploy_folder` options

## [1.0.1] - 2021-12-10
### Fixed
- Fix name of Drupal workflow in Changelog
- Fix deployments not pushing `input.deploy_branch`

## [1.0.0] - 2021-11-26
### Added
- Add Composer setup and install composite action
- Add Drupal CI/CD reusable workflow
- Add WordPress Theme CI/CD reusable workflow

[Unreleased]: https://github.com/projectcosmic/gh-actions/compare/v2.2.0...2.x
[2.2.0]: https://github.com/projectcosmic/gh-actions/compare/v2.1.6...v2.2.0
[2.1.6]: https://github.com/projectcosmic/gh-actions/compare/v2.1.5...v2.1.6
[2.1.5]: https://github.com/projectcosmic/gh-actions/compare/v2.1.4...v2.1.5
[2.1.4]: https://github.com/projectcosmic/gh-actions/compare/v2.1.3...v2.1.4
[2.1.3]: https://github.com/projectcosmic/gh-actions/compare/v2.1.2...v2.1.3
[2.1.2]: https://github.com/projectcosmic/gh-actions/compare/v2.1.1...v2.1.2
[2.1.1]: https://github.com/projectcosmic/gh-actions/compare/v2.1.0...v2.1.1
[2.1.0]: https://github.com/projectcosmic/gh-actions/compare/v2.0.0...v2.1.0
[2.0.0]: https://github.com/projectcosmic/gh-actions/compare/v1.0.1...v2.0.0
[1.0.1]: https://github.com/projectcosmic/gh-actions/compare/v1.0.0...v1.0.1
[1.0.0]: https://github.com/projectcosmic/gh-actions/releases/tag/v1.0.0
[keepachangelog]: https://keepachangelog.com/
[semver]: https://semver.org/spec/v2.0.0.html
