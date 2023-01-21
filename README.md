# <h1 align="center"> Hardhat Foundry Template </h1>

Combines hardhat and foundry testing frameworks to take advantage of coverage and fuzzing capabiltiies, along with their native tools.

## Getting Started

### Requirements

The following will need to be installed. Please follow the links and instructions.

- [Foundry](https://github.com/foundry-rs/foundry)
- yarn or npm >= 7

### Quickstart

1. Install dependencies

Once you've cloned and entered into your repository, you need to install the necessary dependencies. In order to do so, simply run:

```shell
forge install
```

2. Build

```bash
forge build
```

3. Test

```bash
forge test
# or
npx hardhat test
```

For more information on how to use Foundry, check out the [Foundry Github Repository](https://github.com/foundry-rs/foundry/tree/master/forge) or type `forge help` in your terminal.

## Features

### GitHub Templates

The template comes with a list of templates:

- [feature](.github/ISSUE_TEMPLATE/feature.md)
- [bug](.github/ISSUE_TEMPLATE/bug.md)
- [pull request](.github/pull_request_template.md)

### Install Libraries

- Install libraries with Foundry which work with Hardhat.

```bash
forge install openzeppelin/openzeppelin-contracts # just an example
```

### Generate documentation

- Generates and builds an mdbook from Solidity source files.

```bash
forge doc # generates docs in ./docs
forge doc --serve # generates docs and serves them on localhost:3000
```

### Update Gas Snapshots

```sh
forge snapshot
```

### Custom Tasks

- Use Hardhat's task framework

```bash
npx hardhat example
```

## Resources

For more infomation on how to use Foundry features, refer to:

- [forge-std](https://github.com/foundry-rs/forge-std/)
- [cheat codes](https://github.com/foundry-rs/foundry/blob/master/forge/README.md#cheat-codes)
- [Foundry book](https://book.getfoundry.sh/)
