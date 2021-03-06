# @standard-release/app [![npm version][npmv-img]][npmv-url] [![github release][ghrelease-img]][ghrelease-url] [![License][license-img]][license-url]

> GitHub App for creating GitHub Releases, following the [Conventional Commits](https://conventionalcommits.org) and [SemVer](https://semver.org) specifications

Please consider following this project's author, [Charlike Mike Reagent](https://github.com/tunnckoCore), and :star: the project to show your :heart: and support.

<div id="thetop"></div>

[![Code style][codestyle-img]][codestyle-url]
[![CircleCI linux build][linuxbuild-img]][linuxbuild-url]
[![CodeCov coverage status][codecoverage-img]][codecoverage-url]
[![DavidDM dependency status][dependencies-img]][dependencies-url]
[![Renovate App Status][renovateapp-img]][renovateapp-url]
[![Make A Pull Request][prs-welcome-img]][prs-welcome-url]
[![Semantically Released][new-release-img]][new-release-url]

If you have any _how-to_ kind of questions, please read the [Contributing Guide](./CONTRIBUTING.md) and [Code of Conduct](./CODE_OF_CONDUCT.md) documents.  
For bugs reports and feature requests, [please create an issue][open-issue-url] or ping
[@tunnckoCore](https://twitter.com/tunnckoCore) at Twitter.

[![Become a Patron][patreon-img]][patreon-url]
[![Conventional Commits][ccommits-img]][ccommits-url]
[![NPM Downloads Weekly][downloads-weekly-img]][npmv-url]
[![NPM Downloads Monthly][downloads-monthly-img]][npmv-url]
[![NPM Downloads Total][downloads-total-img]][npmv-url]
[![Share Love Tweet][shareb]][shareu]

Project is [semantically](https://semver.org) & automatically released on [CircleCI](https://circleci.com) by itself.

<!-- Logo when needed:

<p align="center">
  <a href="https://github.com/standard-release/app">
    <img src="./media/logo.png" width="85%">
  </a>
</p>

-->

## Table of Contents

- [Install the App](#install-the-app)
- [Usual Flow](#usual-flow)
- [Alternative Flow](#alternative-flow)
- [See Also](#see-also)
- [Contributing](#contributing)
  * [Follow the Guidelines](#follow-the-guidelines)
  * [Support the project](#support-the-project)
  * [OPEN Open Source](#open-open-source)
  * [Wonderful Contributors](#wonderful-contributors)
- [License](#license)

_(TOC generated by [verb](https://github.com/verbose/verb) using [markdown-toc](https://github.com/jonschlinkert/markdown-toc))_

## Install the App

![uptime status](https://badgen.net/uptime-robot/status/m781479241-8659699c878ab68940b6fe8f) 
![uptime day](https://badgen.net/uptime-robot/day/m781479241-8659699c878ab68940b6fe8f) 
![uptime month](https://badgen.net/uptime-robot/month/m781479241-8659699c878ab68940b6fe8f) 
![uptime response](https://badgen.net/uptime-robot/response/m781479241-8659699c878ab68940b6fe8f) 

Install this app on your preferred account: [Standard Release GitHub App](https://github.com/apps/standard-release) 

Automatically publish GitHub releases, based on commits that follows [Conventional Commits](https://conventionalcommits.org) specification.  
Pretty similar to the [Semantic Release](https://github.com/semantic-release), but only an App.

**[back to top](#thetop)**

## Usual Flow

This app works best with it's [@standard-release/cli](https://github.com/standard-release/cli) for npm publishing, but is not limited to it!  
So in case you want to combine both, follow this steps:

1. Install this App
2. Add your `NPM_TOKEN` env variable (needed for the CLI only) in your CI
3. Install [`@standard-release/cli`](https://github.com/standard-release/cli) (as devDependency for example) 
4. Configure your CI to run `standard-release` only on master branch

_Note: If you don't want automatic publish on continuous integration services, but want to run it locally whenever you want, then you should run `standard-release --no-ci` instead. See the cli docs for more info._

## Alternative Flow

Otherwise, you still can use only the App and leave the npm publishing to another tool, for example [semantic-release](https://github.com/semantic-release) or [standard-version][], or Sindre's [np](https://npm.im/np). In this case the step is one: just install that app on your preferred account (your own or to some organization).

Basically, how this app works is pretty simple. It will listen to all CI jobs to finish successfully and then publish a GitHub Release. If some of the CI stuff fail, it won't do anything. The CI detection is based on a [status name check](https://github.com/standard-release/app/blob/1a3e8119d75f7385b354045eeb0858ef94d58720/src/index.js#L12-L19), so it works for Travis, CircleCI, AppVeyor and others.

**[back to top](#thetop)**

## See Also

Some of these projects are used here or were inspiration for this one, others are just related. So, thanks for your existance!

- [asia](https://www.npmjs.com/package/asia): Blazingly fast, magical and minimalist testing framework, for Today and… [more](https://github.com/olstenlarck/asia#readme) | [homepage](https://github.com/olstenlarck/asia#readme "Blazingly fast, magical and minimalist testing framework, for Today and Tomorrow")
- [detect-next-version](https://www.npmjs.com/package/detect-next-version): Calculates next version, based on given commit message and following… [more](https://github.com/tunnckoCoreLabs/detect-next-version) | [homepage](https://github.com/tunnckoCoreLabs/detect-next-version "Calculates next version, based on given commit message and following Conventional Commits")
- [docks](https://www.npmjs.com/package/docks): Extensible system for parsing and generating documentation. It just freaking… [more](https://github.com/tunnckoCore/docks) | [homepage](https://github.com/tunnckoCore/docks "Extensible system for parsing and generating documentation. It just freaking works!")
- [git-commits-since](https://www.npmjs.com/package/git-commits-since): Get all commits since given period of time or by… [more](https://github.com/tunnckoCoreLabs/git-commits-since) | [homepage](https://github.com/tunnckoCoreLabs/git-commits-since "Get all commits since given period of time or by default from latest git semver tag. Understands and follows both SemVer and the Conventional Commits specification.")
- [gitcommit](https://www.npmjs.com/package/gitcommit): Lightweight and joyful `git commit` replacement. Conventional Commits compliant. | [homepage](https://github.com/tunnckoCore/gitcommit "Lightweight and joyful `git commit` replacement. Conventional Commits compliant.")
- [parse-commit-message](https://www.npmjs.com/package/parse-commit-message): Extensible parser for git commit messages following Conventional Commits Specification | [homepage](https://github.com/tunnckoCoreLabs/parse-commit-message "Extensible parser for git commit messages following Conventional Commits Specification")

**[back to top](#thetop)**

## Contributing

### Follow the Guidelines

Please read the [Contributing Guide](./CONTRIBUTING.md) and [Code of Conduct](./CODE_OF_CONDUCT.md) documents for advices.  
For bugs reports and feature requests, [please create an issue][open-issue-url] or ping
[@tunnckoCore](https://twitter.com/tunnckoCore) at Twitter.

### Support the project

[Become a Partner or Sponsor?][patreon-url] :dollar: Check the **Partner**, **Sponsor** or **Omega-level** tiers! :tada: You can get your company logo, link & name on this file. It's also rendered on package page in [npmjs.com][npmv-url] and [yarnpkg.com](https://yarnpkg.com/en/package/@standard-release/app) sites too! :rocket:

Not financial support? Okey! [Pull requests](https://github.com/tunnckoCoreLabs/contributing#opening-a-pull-request), stars and all kind of [contributions](https://opensource.guide/how-to-contribute/#what-it-means-to-contribute) are always
welcome. :sparkles:

### OPEN Open Source

This project is following [OPEN Open Source](http://openopensource.org) model

> Individuals making significant and valuable contributions are given commit-access to the project to contribute as they see fit. This project is built on collective efforts and it's not strongly guarded by its founders.

There are a few basic ground-rules for its contributors

1. Any **significant modifications** must be subject to a pull request to get feedback from other contributors.
2. [Pull requests](https://github.com/tunnckoCoreLabs/contributing#opening-a-pull-request) to get feedback are _encouraged_ for any other trivial contributions, but are not required.
3. Contributors should attempt to adhere to the prevailing code-style and development workflow.

### Wonderful Contributors

Thanks to the hard work of these wonderful people this project is alive! It follows the
[all-contributors](https://github.com/kentcdodds/all-contributors) specification.  
Don't hesitate to add yourself to that list if you have made any contribution! ;) [See how,
here](https://github.com/jfmengels/all-contributors-cli#usage).

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore -->
| [<img src="https://avatars3.githubusercontent.com/u/5038030?v=4" width="120px;"/><br /><sub><b>Charlike Mike Reagent</b></sub>](https://tunnckocore.com)<br />[💻](https://github.com/standard-release/app/commits?author=tunnckoCore "Code") [📖](https://github.com/standard-release/app/commits?author=tunnckoCore "Documentation") [💬](#question-tunnckoCore "Answering Questions") [👀](#review-tunnckoCore "Reviewed Pull Requests") [🔍](#fundingFinding-tunnckoCore "Funding Finding") |
| :---: |

<!-- ALL-CONTRIBUTORS-LIST:END -->

Consider showing your [support](#support-the-project) to them. :sparkling_heart:

## License

Copyright (c) 2017-present, [Charlike Mike Reagent](https://tunnckocore.com) `<mameto2011@gmail.com>` & [contributors](#wonderful-contributors).  
Released under the [Apache-2.0 License][license-url].

<!-- Heading badges -->

[npmv-url]: https://www.npmjs.com/package/@standard-release/app
[npmv-img]: https://badgen.net/npm/v/@standard-release/app?icon=npm

[ghrelease-url]: https://github.com/standard-release/app/releases/latest
[ghrelease-img]: https://badgen.net/github/release/standard-release/app?icon=github

[license-url]: https://github.com/standard-release/app/blob/master/LICENSE
[license-img]: https://badgen.net/npm/license/@standard-release/app

<!-- Front line badges -->

[codestyle-url]: https://github.com/airbnb/javascript
[codestyle-img]: https://badgen.net/badge/code%20style/airbnb/ff5a5f?icon=airbnb

[linuxbuild-url]: https://circleci.com/gh/standard-release/app/tree/master
[linuxbuild-img]: https://badgen.net/circleci/github/standard-release/app/master?label=build&icon=circleci

[codecoverage-url]: https://codecov.io/gh/standard-release/app
[codecoverage-img]: https://badgen.net/codecov/c/github/standard-release/app?icon=codecov

[dependencies-url]: https://david-dm.org/standard-release/app
[dependencies-img]: https://badgen.net/david/dep/standard-release/app?label=deps

[ccommits-url]: https://conventionalcommits.org/
[ccommits-img]: https://badgen.net/badge/conventional%20commits/v1.0.0/dfb317
[new-release-url]: https://github.com/apps/standard-release
[new-release-img]: https://badgen.net/badge/semantically/released/05c5ff

[downloads-weekly-img]: https://badgen.net/npm/dw/@standard-release/app
[downloads-monthly-img]: https://badgen.net/npm/dm/@standard-release/app
[downloads-total-img]: https://badgen.net/npm/dt/@standard-release/app

[renovateapp-url]: https://renovatebot.com
[renovateapp-img]: https://badgen.net/badge/renovate/enabled/green
[prs-welcome-img]: https://badgen.net/badge/PRs/welcome/green
[prs-welcome-url]: http://makeapullrequest.com
[paypal-donate-url]: https://paypal.me/tunnckoCore/10
[paypal-donate-img]: https://badgen.net/badge/$/support/purple
[patreon-url]: https://www.patreon.com/bePatron?u=5579781
[patreon-img]: https://badgen.net/badge/patreon/tunnckoCore/F96854?icon=patreon
[patreon-sponsor-img]: https://badgen.net/badge/become/a%20sponsor/F96854?icon=patreon

[shareu]: https://twitter.com/intent/tweet?text=https://github.com/standard-release/app&via=tunnckoCore
[shareb]: https://badgen.net/badge/twitter/share/1da1f2?icon=twitter
[open-issue-url]: https://github.com/standard-release/app/issues/new

[new-release]: https://github.com/tunnckoCoreLabs/new-release
[semantic-release]: https://github.com/semantic-release/semantic-release
[standard-version]: https://github.com/conventional-changelog/standard-version