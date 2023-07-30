# typescript-utils monorepo

[![npm package][npm-img]][npm-url]
[![Build Status][build-img]][build-url]
[![Downloads][downloads-img]][downloads-url]
[![Issues][issues-img]][issues-url]
[![Code Coverage][codecov-img]][codecov-url]
[![Commitizen Friendly][commitizen-img]][commitizen-url]
[![Semantic Release][semantic-release-img]][semantic-release-url]

## Features

This monorepo encompasses 1 utility `@vllc/tsc-diff` which is used to run eslint and jest. There are two packages specific to eslint and jest to make running pre-commit and pre-push hooks easier. `@vllc/tsc-diff` also fully supports being run in isolatation and piping changes to custom test runners.

If you have a tool/test-runner that you think needs to be supported please file an issue and consider contributing to add support for this tool.

- Adds the ability to run tsc with your project's current config but only include specific files.
- [@vllc/tsc-diff](./packages/tsc-diff) - main package, compiles only staged files
- [@vllc/tsc-diff-eslint](./packages/tsc-diff) - eslint support
- [@vllc/tsc-diff-jest](./packages/tsc-diff) - jest support
  - Adds a compatibility script to directly mutate the tsconfig.json file (with backups) for babel-jest, which may work well with esbuild and swc-jest
  - Adds wrapper around jest so it runs `ts-jest` with the staged tsconfig file.

## Getting started

> typescript-utils monorepo packages

## Install

> @vllc/tsc-diff-eslint

Install this package for eslint to run tsc only on the test files dependency tree.

```bash
npm install -D @vllc/tsc-diff-eslint
```

> @vllc/tsc-diff-jest

Install this package for jest to run tsc only on the test files dependency tree

```bash
npm install -D @vllc/tsc-diff-jest
```

> @vllc/tsc-diff

Install this package for getting the staged and upstream diff file output with flexibility such as `@vllc/tsc-diff start` and `@vllc/tsc-diff stop` to cleanup the dynamic tsconfig.json file generated.

```bash
npm install -D @vllc/tsc-diff
```

## Usage

WIP

## API

WIP, this will be dynamically generated

### tsc-diff(input, options?)

#### input

Type: `string`

Lorem ipsum.

#### options

Type: `object`

##### postfix

Type: `string`
Default: `rainbows`

[build-img]: https://github.com/VirtualizeLLC/typescript-utils/actions/workflows/release.yml/badge.svg
[build-url]: https://github.com/VirtualizeLLC/typescript-utils/actions/workflows/release.yml
[downloads-img]: https://img.shields.io/npm/dt/typescript-npm-package-template
[downloads-url]: https://www.npmtrends.com/typescript-npm-package-template
[npm-img]: https://img.shields.io/npm/v/typescript-npm-package-template
[npm-url]: https://www.npmjs.com/package/typescript-npm-package-template
[issues-img]: https://img.shields.io/github/issues/VirtualizeLLC/typescript-utils
[issues-url]: https://github.com/VirtualizeLLC/typescript-utils/issues
[codecov-img]: https://codecov.io/gh/VirtualizeLLC/typescript-utils/branch/main/graph/badge.svg
[codecov-url]: https://codecov.io/gh/VirtualizeLLC/typescript-utils
[semantic-release-img]: https://img.shields.io/badge/%20%20%F0%9F%93%A6%F0%9F%9A%80-semantic--release-e10079.svg
[semantic-release-url]: https://github.com/semantic-release/semantic-release
[commitizen-img]: https://img.shields.io/badge/commitizen-friendly-brightgreen.svg
[commitizen-url]: http://commitizen.github.io/cz-cli/
