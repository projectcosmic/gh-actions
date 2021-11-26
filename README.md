# GitHub Actions & Workflows

This repository contains reusable GitHub actions and workflows primarily for
continuous integration and deployment workflows of
[Project Cosmic Limited GitHub repositories][gh-cosmic].

## Actions

### [Composer Setup & Install](.github/actions/setup-composer-install/action.yml)

Sets up [composer][composer] and runs `composer install`. The project must have
a `composer.json` at the root of the project. The action should be run in an
environment where the `update-alternatives` command is available as this is used
to set the PHP version.

## Workflows

### [WordPress Theme CI/CD](.github/workflows/wordpress-theme-ci-cd.yml)

Runs CI and CD for a [WordPress][wordpress] theme. The project must have a
`composer.json` at the root of the project. If `with.assets` is `true` (the
default), then the project must also have a `package.json` (from [npm][npm]) in
the root. This must also have a [`volta.node`][volta] present for the workflow
to set up the correct [`node`][nodejs] version.

When deploying, the workflow assumes the theme folder in production is
`<with.deploy_folder>/wp-content/themes/<github_repository_name>`.

[composer]: https://getcomposer.org/
[gh-cosmic]: https://github.com/projectcosmic/
[npm]: https://docs.npmjs.com/files/package.json/
[nodejs]: https://nodejs.org/
[volta]: https://volta.sh/
[wordpress]: https://wordpress.org/
