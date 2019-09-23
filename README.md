# JCC Design System

Based on the [Pattern Lab Twig Standard Edition for Drupal](https://github.com/pattern-lab/edition-php-drupal-standard).

## Prerequisites

- [`composer`](https://getcomposer.org) installed globally
- Node v12.x.x

## Getting Started

1. `git clone https://github.com/Exygy/courtyard.git` to create the project directory.
1. `cd courtyard` to go to the directory.
1. `composer install` to install Pattern Lab.
   - Answer `M` to all questions of the format `the path ./source/_twig-components/[directory name] already exists. merge or replace with the contents of pattern-lab/drupal-twig-components package?`
   - Answer `Y` to `update the config option styleguideKitPath (/[path to your repo]/vendor/pattern-lab/styleguidekit-twig-default) with the value vendor/pattern-lab/styleguidekit-twig-default?`
1. `npm install`
1. `npm run start` to generate the pattern library, watch for changes, and serve the pattern library on `localhost` at a port that will be specified in the command's console output.

## To update Pattern Lab

    composer update

## Deployment

You can view a public deployment of the pattern library at https://confident-allen-d061ed.netlify.com/. This is hosted on an Exygy Netlify account. The Netlify deployment autodeploys the master branch from this repo. Each time a commit is pushed to the master branch, Netlify will run the `npm run build` command to build the pattern library, and it will then deploy that new build from the `public` directory.

Netlify will also create a preview deployment for each PR created in this repo. To view the preview deployment for a PR, go to the PR and scroll down to the bottom to the checks section. In that section, there is a list item for the deploy preview. Click the "Details" link in that list item to view the deploy preview (see below image).

<img src="./netlify-pr-deploy.png?raw=true" height="300" >

## Contributing

### Code Style

We use the automatic code formatter Prettier. If you use an IDE such as Sublime Text, VSCode, or similar, you can likely add a Prettier extension that will autoformat your files using Prettier rules on file save. If you're not using an IDE that integrates with it, you should run `npx prettier --write [filepath]` on all added or changed files before you submit a pull request.
