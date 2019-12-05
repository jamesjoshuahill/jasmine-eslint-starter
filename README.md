# jasmine-eslint-starter

This is a guide for setting up a new project to practise test-driving JavaScript
using:
- [Jasmine Standalone](https://jasmine.github.io/) for testing
- [ESLint](https://eslint.org/) for linting

## One-off set up

### Install ESLint

1. Install ESLint using Homebrew
    ```
    $ brew install eslint
    ```

### Install ESLint package in Atom

1. Install `linter-eslint` package for Atom
    - Go to Atom > Preferences > Install
    - Search for the `linter-eslint` package
    - Click Install

1. Configure `linter-eslint` package
    - Go to Atom > Preferences > Packages
    - Search for the `linter-eslint` package
    - Click Settings
    - Check `Use global ESLint installation`


## Start a new project

1. Create a directory for your new project

    For example:
    ```
    $ mkdir -p ~/projects/fizzbuzz-js
    $ cd ~/projects/fizzbuzz-js
    ```

1. Install [Jasmine Standalone](https://jasmine.github.io/pages/getting_started.html)

    At the time of writing the latest version was `3.5.0`. The following commands
    will download the release and unzip it.
    ```
    $ curl -O -L https://github.com/jasmine/jasmine/releases/download/v3.5.0/jasmine-standalone-3.5.0.zip
    $ unzip jasmine-standalone-3.5.0.zip
    ```

1. Copy the basic ESLint configuration into your project
    ```
    $ curl -O https://raw.githubusercontent.com/jamesjoshuahill/jasmine-eslint-starter/master/.eslintrc.json
    ```

1. Open Atom in your new project
    ```
    $ atom .
    ```

1. Open `spec/PlayerSpec.js` and you should see two ESLint warnings in your editor:
    ```
    'Player' is not defined (no-undef)
    'Song' is not defined (no-undef)
    ```
    These warnings are expected and you can ignore them.

    > ℹ️ These warnings occur because ESLint does not read the `<script>` tags in
    > `SpecRunner.html` that load `Player.js` and `Song.js`.

1. Open `SpecRunner.html` to run the tests
    ```
    $ open SpecRunner.html
    ```
