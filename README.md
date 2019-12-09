# jasmine-eslint-starter

This is a guide for setting up a new project to practise test-driving JavaScript
using:
- [Jasmine Standalone](https://jasmine.github.io/) for testing
- [ESLint](https://eslint.org/) for linting

## One-off set up

### Install ESLint

1. Install ESLint using Homebrew
    ```bash
    $ brew install eslint
    ```

### Install ESLint package in Atom

1. Install `linter-eslint` package for Atom
    - Go to **Atom > Preferences > Install**
    - Search for the `linter-eslint` package
    - Click **Install**

## Start a new project

1. Create a directory for your new project

    For example:
    ```bash
    $ mkdir YOUR_PROJECT_NAME
    $ cd YOUR_PROJECT_NAME
    ```

1. Install [Jasmine Standalone](https://jasmine.github.io/pages/getting_started.html)

    At the time of writing the latest version was `3.5.0`.
    ```bash
    # Download Jasmine Standalone
    $ curl -O -L https://github.com/jasmine/jasmine/releases/download/v3.5.0/jasmine-standalone-3.5.0.zip

    # Unzip files
    $ unzip jasmine-standalone-3.5.0.zip
    ```

1. Download a [basic ESLint configuration](https://github.com/jamesjoshuahill/jasmine-eslint-starter/blob/master/.eslintrc.json)
    ```bash
    $ curl -O https://raw.githubusercontent.com/jamesjoshuahill/jasmine-eslint-starter/master/.eslintrc.json
    ```

1. Open Atom in your new project
    ```bash
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
    ```bash
    $ open SpecRunner.html
    ```

1. Your new project structure should be
    ```
    .
    ├── MIT.LICENSE
    ├── SpecRunner.html
    ├── lib
    │   └── jasmine-3.5.0
    │       └── ...
    ├── spec
    │   ├── PlayerSpec.js
    │   └── SpecHelper.js
    └── src
        ├── Player.js
        └── Song.js
    ```

1. Now, you can start test-driving by creating a new spec!
