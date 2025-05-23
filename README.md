# AB Improvement Proposals (AIPs)

[![Join the chat at https://gitter.im/ABFoundationGlobal/AIPs](https://badges.gitter.im/ABFoundationGlobal/AIPs.svg)](https://gitter.im/ABFoundationGlobal/AIPs?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge) ![Deploy Status](https://img.shields.io/github/workflow/status/ABFoundationGlobal/AIPs/Deploy%20Github%20Pages/main)

AB Improvement Proposals (AIPs) describe Proposals for the AB including _Economic Model_, _Personnel_, _Technical_, _Community Governance_ and _Business_.

We welcome anyone with suggestions related to AB to compile a AIP.

This repository tracks the ongoing status of AIPs.

- [AIPs Website](https://aips.ab.org/) is built from AIPs and Docs from this repository.

- [All AIPs](https://aips.ab.org/aips/) displays all AIPs merged into this repository, source files are located under `AIPS` directory.

- [AIP Process](https://aips.ab.org/guides/aip-process/) that governs the AIPs repository.

## Contributing to AIPs

AB Improvement Proposals (AIPs) repository exists as a place to share concrete proposals with potential users of the proposal and the Newton community at large.

Visit [AIP Guidelines](https://aips.ab.org/guides/) to learn how to contribute to AIPs.

Docs for Guides are located in `./guides` directory in this repository.

## Local Development

### Prerequisites

1. Open Terminal.

2. Check whether you have NodeJS and Yarn installed:

```bash
node --version && yarn --version
```

If you don't have NodeJS or Yarn installed, install them from [NodeJS Download](https://nodejs.org/en/download/) and [Yarn Installation](https://yarnpkg.com/getting-started/install).

3. Recursively clone this repository as it contains a submodule.

```bash
git clone --recursive https://github.com/ABFoundationGlobal/AIPs.git
```

If not cloned with `--recursive`, update submodule to fetch submodule:

```bash
git submodule update --init --recursive
```

4. Install Dependencies:

```bash
yarn
```

### Start Website in Dev Mode

```bash
yarn dev
```

### Build Website Files

```bash
yarn build
```

### Check Markdown Format Before Making A Commit

We use prettier to check and format Markdown documents.

It is recommended to check your format before making a commit.

**Format Check**

```bash
yarn fc
```

**Format Fix:** this will help clean the format

```bash
yarn ff
```

## License

- The AIPs and Docs  in this repostitory are licensed under the [CC0 1.0 Universal (CC0 1.0)
Public Domain Dedication](https://creativecommons.org/publicdomain/zero/1.0/).

- The underlying program used to build the website is licensed under the [Apache License 2.0](http://www.apache.org/licenses/LICENSE-2.0).

- Individule files may contains seperated License, those files should use their own Licenses.
