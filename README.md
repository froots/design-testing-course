# Design testing course example project

This project is a companion project for the free email course on design testing available on tinnedfruit.com. It won't make much sense unless you have signed up for that.

## Pre-requisites

Before you run this project, you'll need:

* A GitHub account - to fork and clone this repository
* [Git](https://git-scm.com/) - Because Git
* [Node.JS and NPM](https://nodejs.org/) - to install dependencies and run commands

### WebDriver implementations

By default, layout tests will run on Chrome and PhantomJS. You'll need to install WebDriver implementations for these to work, otherwise you will get errors when you run tests. Follow the installation instructions on the respective sites:

* [Chromedriver](https://sites.google.com/a/chromium.org/chromedriver/)
* [PhantomJS](http://phantomjs.org/)

Alternatively, if you are using MacOS and have Homebrew installed, you can run `brew install phantomjs chromedriver` from a terminal prompt.

You might also try running tests using Firefox by adding another check command in the `suite.test` file. Unfortunately Firefox is tricky at the time of writing because Mozilla is in the process of separating the WebDriver implementation from the core Firefox download. Firefox version 48 and higher do not bundle a WebDriver.

## Installation

Once you have the pre-requisites, follow these steps:

1. Fork this repository to your own GitHub account.
2. Clone the repository to your own computer.
3. From a command prompt, `cd` into the project and run `npm install` to install the project dependencies

## Scripts

Here are the NPM scripts that can be run for this project:

* `npm run serve` - starts a web server on port 8080. It also opens the home page in a browser for you.
* `npm run stylelint` - runs the [stylelint](http://stylelint.io/) CSS linter over all CSS files in the `src/css` directory.
* `npm test` - runs Galen Framework layout tests using the `test/suite.test` suite and the `test/feature.gspec` spec files. You'll need to have the web server running first (run `npm run serve` in another terminal window)
* `npm run report` - opens the Galen test report from `test/report/report.html` in a browser window. This will only work after a test run.

## Help!

If you need any help with anything, raise an issue on GitHub or email me on [james@tinnedfruit.com](mailto:james@tinnedfruit.com).