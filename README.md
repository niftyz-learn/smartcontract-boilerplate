# Solidity Smart Contract boilerplate based on HardHat

With this boilerplate you'll be able to create even more automations than standard hardhat example, we'll added also the possibility to add a block explorer by running Blockscout using Docker.

## Requirements

You will need `NodeJS` and `YARN` installed in your machine, if you're ready to start just install dependencies with:

```
yarn
```

Optionally you will need `Docker` and `Docker Compose` to run the block explorer.

## Init local network

To init a new hardhat network you'll need to run:
```
yarn network
```

With this command a new `hardhat.json` file will be created, a new mnemonic will be created (don't use default one in any case) and a new hardhat network will run. Leave this terminal opened and open a new one.

## Deploy contract

To deploy the contract simply run:

```
yarn task deploy hardhat
```

With this command we're saying the `scripts/_task.js` to run the `scripts/deploy.js` file using `configs/hardhat.json` file.

## Run other scripts

As you can easily understand you're now able to write your own scripts (or tests) and use it like:

```
yarn task myscript hardhat
```

or you can change the `hardhat` with `goerli` (for instance) and deploy to Rinkeby network. Of course you will need to setup your own `provider` inside the `configs/goerli.json` file adding an Alchemy, Infura or whatsoever provider.

## Run block explorer

First of all use the command `yarn explorer:init` to download the block explorer. You will need to have both `Docker` and `Docker Compose` installed on your machine.
Then you can start and stop the explorer using:

Be sure to have the network running before starting the explorer.

```
yarn explorer:start
yarn explorer:stop
```

Each time you stop and start the explorer you will also need to restart the network.