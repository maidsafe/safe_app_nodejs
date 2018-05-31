# safe_app_nodejs

A safe_app library for [Node.js](https://nodejs.org/).

**Maintainer:** Gabriel Viganotti (gabriel.viganotti@maidsafe.net)

|Linux/OS X|Windows|Coverage Status|
|:---:|:---:|:---:|
|[![Build Status](https://travis-ci.org/maidsafe/safe_app_nodejs.svg?branch=master)](https://travis-ci.org/maidsafe/safe_app_nodejs)|[![Build status](https://ci.appveyor.com/api/projects/status/efktyecwydxrhs5d/branch/master?svg=true)](https://ci.appveyor.com/project/MaidSafe-QA/safe-app-nodejs/branch/master)|[![Coverage Status](https://coveralls.io/repos/github/maidsafe/safe_app_nodejs/badge.svg)](https://coveralls.io/github/maidsafe/safe_app_nodejs)|

## API Documentation

The documentation for the safe_app Node.js API is available at <http://docs.maidsafe.net/safe_app_nodejs/>.

## Development

1. Prerequisites

    * [Node.js](https://nodejs.org) ^8.0.0 (we recommend installing it via [nvm](https://github.com/creationix/nvm))
    * [Git](https://git-scm.com/)
    * [Yarn](https://yarnpkg.com) (as a replacement for `npm`).

2. Clone this GitHub repository:

    ```bash
    git clone https://github.com/maidsafe/safe_app_nodejs.git
    ```

3. Install the dependencies:

    ``` bash
    cd safe_app_nodejs
    yarn
    ```

    If you are working on a development environment, you can run `NODE_ENV=dev yarn` instead in order to get the [`safe_app`](https://github.com/maidsafe/safe_client_libs/tree/master/safe_app) library which uses the `MockVault` file rather than connecting to the actual SAFE Network.

### Testing

To run the tests locally, make sure you installed the [`safe_app`](https://github.com/maidsafe/safe_client_libs/tree/master/safe_app) library with `NODE_ENV=dev yarn`, then you can run them by executing `yarn test`.

Note: If you are compiling your own [`safe_app`](https://github.com/maidsafe/safe_client_libs/tree/master/safe_app) library for testing purposes, and if you want to be able to run the tests, make sure to include `testing` in your build features when compiling `safe_app` in `safe_client_libs`, i.e. `cargo build --release --features "use-mock-routing testing"`.

### Mobile Development
If you do not require [system_uri](https://github.com/maidsafe/system_uri) and would like to prevent it from downloading, first set the `PLATFORM_TYPE=mobile` environment variable before running `yarn`.

## Further Help

You can discuss development-related questions on the [SAFE Dev Forum](https://forum.safedev.org/).
Here's a good post to get started: [How to develop for the SAFE Network](https://forum.safedev.org/t/how-to-develop-for-the-safe-network-draft/843).

## License

This SAFE Network library is dual-licensed under

* the Modified BSD ([LICENSE-BSD](https://opensource.org/licenses/BSD-3-Clause)) or
* the MIT license ([LICENSE-MIT](http://opensource.org/licenses/MIT))

at your option.

## Contribution

Copyrights in the SAFE Network are retained by their contributors. No copyright assignment is required to contribute to this project.
