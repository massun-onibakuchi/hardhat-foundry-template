# <h1 align="center"> Hardhat Foundry Template </h1>

Highly opinionated template for smart contract development.

Combines hardhat and foundry testing frameworks to take advantage of coverage and fuzzing capabiltiies, along with their native tools.

## Getting Started

### Requirements

The following will need to be installed. Please follow the links and instructions.

- [Foundry](https://github.com/foundry-rs/foundry)
- Node >= 14
- yarn or npm >= 7

### Quickstart

1. Install dependencies

Once you've cloned and entered into your repository, you need to install the necessary dependencies. In order to do so, simply run:

```shell
yarn install
forge install
```

2. Build

```bash
forge build
```

3. Test

```bash
forge test -vvv
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

### GitHub Actions

- [CI](.github/workflows/ci.yml)

  - Lint
  - Test
  - Coverage
    - Show coverage report in the workflow summary
    - Set `secrets.CODECOV_TOKEN` on GitHub for visualizing coverage report to [codecov.io](https://about.codecov.io/product/features/) (NOTE: the secrets is not required for public repo)

- [Static Analyzer](.github/workflows/slither.yml) ([Slither](https://github.com/crytic/slither))
  - To enable the upload of the SARIF file to GitHub, Requires to be public repo or GitHub Enterprise Cloud user.

### Install Libraries

- Install libraries with Foundry which work with Hardhat.

```bash
forge install openzeppelin/openzeppelin-contracts # just an example
```

And then update remappings in `foundry.toml`.

```
remappings = [
    "@openzeppelin/=lib/openzeppelin-contracts/",
]
```

This will allow you to import libraries like this:

```solidity
// Instead of import "lib/openzeppelin-contracts/token/ERC20/ERC20.sol";
import '@openzeppelin/contracts/token/ERC20/ERC20.sol';
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

### Coverage

```sh
forge coverage
```

### Custom Tasks

- Use Hardhat's task framework

```bash
npx hardhat example
```

### Utility Commands

- Use `cast` command which is a swiss army knife for smart contract development. Type `cast --help` for more information.

#### Tracing a tx

Runs a published transaction in a local environment and prints the trace.

```bash
cast run <txhash> --rpc-url <rpc-url>
```

### Deplyment

See [deployment](./deployment.md)

## Resources

For more infomation on how to use Foundry features, refer to:

- [forge-std](https://github.com/foundry-rs/forge-std/)
- [cheat codes](https://github.com/foundry-rs/foundry/blob/master/forge/README.md#cheat-codes)
- [Foundry book](https://book.getfoundry.sh/)

### Acknowledgements

- [OpenSea/Seaport](https://github.com/ProjectOpenSea/seaport)
- [Primitive Finance/hardhat-foundry](https://github.com/primitivefinance/hardhat-foundry)
