# Contributing to Studio
There are many ways to contribute to Studio project: logging bugs, submitting pull requests, reporting issues, and creating suggestions.

After cloning and building the repo, check out the [issues list](https://github.com/SuperblocksHQ/studio/issues?utf8=%E2%9C%93&q=is%3Aopen+is%3Aissue)

## Build and Run

If you want to understand how Studio works or want to debug an issue, you'll want to get the source, build it, and run the tool locally.

### Getting the sources

```
git clone https://github.com/SuperblocksHQ/studio.git
```

### Prerequisites

- [Git](https://git-scm.com)
- [Node.JS](https://nodejs.org/en/), `>= 8.9.1, < 9.0.0`
- [Yarn](https://yarnpkg.com/en/), follow the [installation guide](https://yarnpkg.com/en/docs/install)

Finally, install all dependencies using `Yarn`:

```
cd studio
yarn
```

### Build

From a terminal, where you have cloned the `studio` repository, execute the following command to run the TypeScript incremental builder:

```bash
yarn run watch
```

Webpack will do an initial full build and will display a message that includes the phrase "Compiled successfully!" and provide you with the ip addresses once the initial build is complete. The builder will then continue to run in the terminal. It will watch for file changes and compile those changes incrementally, giving you a fast, iterative coding experience.

#### Errors and Warnings
Errors and warnings will show in the console while developing Studio. Also make sure to check the developer console of any of the browsers supported in order to check out for console logs and errors.

### Run

To run the application simply execute the following command:

`yarn start`


### Automated Testing
Run the unit tests directly from a terminal by running `yarn run test` from the `studio` folder.


### Linting
We use [eslint](https://eslint.org/) for linting our sources. **NOTE:** We highly recommend you install a eslint helper extension or plugin into your IDE to make sure you can get instant feedback while developing the code.


## Work Branches
Even if you have push rights on the Superblocks/studio repository, you should create a personal fork and create feature branches there when you need them. This keeps the main repository clean and your personal workflow cruft out of sight.

## Pull Requests
To enable us to quickly review and accept your pull requests, always create one pull request per issue and [link the issue in the pull request](https://github.com/blog/957-introducing-issue-mentions). Never merge multiple requests in one unless they have the same root cause. Make sure to keep code changes as small as possible. Avoid pure formatting changes to code that has not been modified otherwise. Pull requests should contain tests whenever possible.

### Where to Contribute
Check out the [full issues list](https://github.com/SuperblocksHQ/studio/issues?utf8=%E2%9C%93&q=is%3Aopen+is%3Aissuee) for a list of all potential areas for contributions. Note that just because an issue exists in the repository does not mean we will accept a contribution to the core editor for it. There are several reasons we may not accepts a pull request like:

* User experience - Since we want to deliver a *easy to use* code editor, the UX should feel lightweight as well and not be cluttered. Most changes to the UI should go through the issue owner and/or the UX team.
* Architectural - The team and/or feature owner needs to agree with any architectural impact a change may make. But of course, feel free to open an issue and make sure we can start a conversation about it!

To improve the chances to get a pull request merged you should select an issue that is labelled with the [`help-wanted`](https://github.com/SuperblocksHQ/studio/labels/help%20wanted) or [`bug`](https://github.com/SuperblocksHQ/studio/labels/bug) labels. If the issue you want to work on is not labelled with `help-wanted` or `bug`, you can start a conversation with the issue owner asking whether an external contribution will be considered.


## Suggestions
We're also interested in your feedback for the future of Studio. You can submit a suggestion or feature request through the issue tracker. To make this process more effective, we're asking that these include more information to help define them more clearly.

## Translations
We appreciate your localization contributions, either by providing new translations, voting on translations, or suggesting process improvements. Currently we are not supporting anything but English but this will change once we introduce i18n to the project.

## Discussion Etiquette

In order to keep the conversation clear and transparent, please limit discussion to English and keep things on topic with the issue. Be considerate to others and try to be courteous and professional at all times.