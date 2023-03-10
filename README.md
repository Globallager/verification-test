# <h1 align="center"> hello-noir: Hardhat x Foundry Template </h1>

Demo hosted on: https://hello-noir.netlify.app/

## Run Tests Step-by-Step

0. `git submodule update --init --recursive`
1. `npm install`
2. `npx hardhat test`
3. Modify Code (circuits/src/main.nr & Prover.toml etc.)
4. `npx hardhat run scripts/generate_sol_verifier.ts`
5. `npx hardhat test`

The frontend repo is a submodule under `ui/`.

---

**Template repository for getting started quickly with Hardhat and Foundry in one project**

![Github Actions](https://github.com/devanonon/hardhat-foundry-template/workflows/test/badge.svg)

### Getting Started

- Use Foundry:

```bash
forge install
forge test
```

- Use Hardhat:

```bash
npm install
npx hardhat test
```

### Features

- Write / run tests with either Hardhat or Foundry:

```bash
forge test
# or
npx hardhat test
```

- Use Hardhat's task framework

```bash
npx hardhat example
```

- Install libraries with Foundry which work with Hardhat.

```bash
forge install rari-capital/solmate # Already in this repo, just an example
```

### Notes

Whenever you install new libraries using Foundry, make sure to update your `remappings.txt` file by running `forge remappings > remappings.txt`. This is required because we use `hardhat-preprocessor` and the `remappings.txt` file to allow Hardhat to resolve libraries you install with Foundry.
