# Jonas Renault's personnal website

[![Jekyll](https://img.shields.io/gem/v/jekyll?label=jekyll)](https://jekyllrb.com/)
[![Ruby gem](https://img.shields.io/gem/v/minimal-mistakes-jekyll?label=minimal%20mistakes)](https://rubygems.org/gems/minimal-mistakes-jekyll)

This is the repository for my personal website. Visit it at [https://jrenault.fr](https://jrenault.fr)

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

Take a look at Minimal Mistakes' [documentation](https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/) for setup and customization of the website.

## Deploy to Github Pages

This website is deployed to Github Pages using a custom [Github Actions workflow](./.github/workflows/jekyll.yml). Follow the steps [here](https://jekyllrb.com/docs/continuous-integration/github-actions/#setting-up-the-action) to setup a deployment for your github pages.

I deployed my website on a custom domain; if you want to deploy it to a default github pages domain instead, delete the [CNAME](./CNAME) file, and update the `domain` and `url` variables in [_config.yml](./_config.yml).

## Google Analytics

Google Analytics is enabled using Minimal Mistakes' [support](https://mmistakes.github.io/minimal-mistakes/docs/configuration/#analytics). To avoid sharing the tracking id on github, the `__GA_TRACKING_ID__` variable in [_config.yml](./_config.yml) is replaced during deployment to Github Pages in the [workflow](./.github/workflows/jekyll.yml). To function properly, you must create a `build` environment in your repository, and [add a secret variable](https://docs.github.com/en/actions/security-guides/using-secrets-in-github-actions#creating-secrets-for-an-environment) named `GA_TRACKING_ID` with the Google Analytics tracking id value.