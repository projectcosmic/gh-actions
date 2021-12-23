# GitHub Actions & Workflows

This repository contains reusable GitHub actions and workflows primarily for
continuous integration and deployment workflows of
[Project Cosmic Limited GitHub repositories][gh-cosmic].

## Actions

### [Composer Setup & Install](.github/actions/setup-composer-install/action.yml)

Sets up [Composer][composer] and runs `composer install`. The project must have
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
`/wp-content/themes/<github_repository_name>`. The deploy target is parsed from
the `@live` [wp-cli site alias][wp-cli-alias].

### [Drupal CI/CD](.github/workflows/drupal-ci-cd.yml)

Runs CI and CD for a [Drupal][drupal] site. The project must be a
[Composer][composer]-managed Drupal project, via
[`drupal/recommended-project`][drupal-recommended] or similar.

If `with.assets` is `true` (the default) then the project must have a
`package.json` (from [npm][npm]) in
`public_html/themes/custom/<github_repository_name>`. This must also have a
[`volta.node`][volta] present for the workflow to set up the correct
[`node`][nodejs] version.

For [PHPUnit][phpunit] tests, one can add
`allowed_test_deprecations-<type>.json` files for
[Symfony PHPUnit Bridge baseline deprecations file][phpunit-bridge-baseline]
where `<type>` is the type declared in the JSON string of `with.php_unit`.

The workflow uses the SSH connection details defined by the `@live`
[Drush site alias][drush-alias] as the deploy target.

### [Drupal Dependabot PR Config Update](.github/workflows/drupal-dependabot-config-update.yml)

Runs any Drupal configuration updates for a dependabot update PR. Must have
`contents: write` and be called on the `pull_request` event.

[composer]: https://getcomposer.org/
[drupal]: https://www.drupal.org/
[drupal-recommended]: https://www.drupal.org/docs/develop/using-composer/starting-a-site-using-drupal-composer-project-templates#s-drupalrecommended-project
[drush-alias]: https://www.drush.org/latest/site-aliases/
[gh-cosmic]: https://github.com/projectcosmic/
[phpunit]: https://phpunit.de/
[phpunit-bridge-baseline]: https://symfony.com/doc/current/components/phpunit_bridge.html#baseline-deprecations
[npm]: https://docs.npmjs.com/files/package.json/
[nodejs]: https://nodejs.org/
[volta]: https://volta.sh/
[wordpress]: https://wordpress.org/
[wp-cli-alias]: https://make.wordpress.org/cli/handbook/guides/running-commands-remotely/#aliases
