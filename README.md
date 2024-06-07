# Jonas Renault's personnal website

[![Jekyll](https://img.shields.io/badge/jekyll-%3E%3D%203.7-blue.svg)](https://jekyllrb.com/)
[![Ruby gem](https://img.shields.io/gem/v/minimal-mistakes-jekyll.svg)](https://rubygems.org/gems/minimal-mistakes-jekyll)

This is the repository for my personal website. Visit it at [https://jonasrenault.github.io](https://jonasrenault.github.io)

## Credits

The website is based on Michael Rose's [Minimal Mistakes](https://github.com/mmistakes/minimal-mistakes) Jekyll theme.

## Usage

To setup an environment to run the website in development, execute

```console
bundle install
```

then

```console
bundle exec jekyll serve --incremental
```

to serve the website locally and watch changes.

## Documentation

Take a look at Minimal Mistakes' [documentation]((https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/)) for setup and customization of the website.

## Deploy to Github Pages

By default, this website is deployed to Github Pages using a custom Github Actions workflow. Follow the steps [here](https://jekyllrb.com/docs/continuous-integration/github-actions/#setting-up-the-action) to setup a deployment for your github pages.

## Google Analytics

Google Analytics is enabled using Minimal Mistakes' [support](https://mmistakes.github.io/minimal-mistakes/docs/configuration/#analytics). To avoid sharing the tracking id on github, the `__GA_TRACKING_ID__` variable in [_config.yml](./_config.yml) is replaced during deployment to Github Pages in the [workflow](./.github/workflows/jekyll.yml). To function properly, you must create a `build` environment in your repository, and [add a secret variable](https://docs.github.com/en/actions/security-guides/using-secrets-in-github-actions#creating-secrets-for-an-environment) named `GA_TRACKING_ID` with the Google Analytics tracking id value.