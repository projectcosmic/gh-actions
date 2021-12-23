# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog][keepachangelog] and this project
adheres to [Semantic Versioning][semver].

## [Unreleased]
### Changed
- Adjust dependabot context check to push events

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

[Unreleased]: https://github.com/projectcosmic/gh-actions/compare/v2.1.1...3.x
[2.1.1]: https://github.com/projectcosmic/gh-actions/compare/v2.1.0...v2.1.1
[2.1.0]: https://github.com/projectcosmic/gh-actions/compare/v2.0.0...v2.1.0
[2.0.0]: https://github.com/projectcosmic/gh-actions/compare/v1.0.1...v2.0.0
[1.0.1]: https://github.com/projectcosmic/gh-actions/compare/v1.0.0...v1.0.1
[1.0.0]: https://github.com/projectcosmic/gh-actions/releases/tag/v1.0.0
[keepachangelog]: https://keepachangelog.com/
[semver]: https://semver.org/spec/v2.0.0.html
