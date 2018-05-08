# CryptoHackers
CryptoHackers is an example application running on top of the Quorum network and allows users to buy and sell virtual hackathon gear. It demonstrates how to run an simple Ethereum application and how to write simple Smart Contracts that interact with the Ethereum-based network.

Once you have your Quorum network running, you can run the CryptoHackers application locally by opening a new terminal window (this time outside the vagrant instance). Open the project directory and install the dependencies.

## Requirements
* Install [NodeJS](https://nodejs.org) - Event-driven Javascript runtime environment
* Install [NPM](https://www.npmjs.com/) - Popular package manager for JavaScript
* Install [Truffle](http://truffleframework.com/) - Development framework for Ethereum applications

## Installation
```sh
$ cd cryptohackers/
$ npm install

```
## Running
To get your CryptoHackers application up and running locally, you will need to compile your contracts, migrate those contracts to the network, populate those contracts with data, then run your application:

```sh
$ truffle compile
$ truffle migrate
$ npm run seed
$ npm start
```
## Commands
Inside the CryptoHackers project, you can run some built-in commands:

### `npm start` or `yarn start`
Runs the app in development mode.<br>
Open [http://localhost:8000](http://localhost:8000) to view it in the browser.

The page will automatically reload if you make changes to the code.<br>
You will see the build errors and lint warnings in the console.

### `npm run compile` or `truffle compile`
Compiles the Solidity contracts (files with the `.sol` extension) in the `contracts/` directory. This is necessary to run every time you make a change to one of the contracts. Truffle will only compile the contracts that were changed since the last compile.

Compiled versions of these contracts will be placed in the `build/contracts/` directory.

Additional [documentation](http://truffleframework.com/docs/getting_started/compile).

### `npm run migrate` or `truffle migrate`
Migrations are JavaScript files that deploy your compiled contracts to the Ethereum network. To see your contract on the network, you must run `truffle migrate` after you run the network.

All migrations are located within the `migrations/` directory. To add a new contract to the network, you must add it to the `migrations/2_deploy_contract.js` file or create a new migration file.

Additional [documentation](http://truffleframework.com/docs/getting_started/migrations)

### `npm run seed` or `truffle exec seed.js`
Once your contracts are live on the network, you need to seed the network with default data. We do this by running the `seed.js` script which populates our contract with data from `hackers.json`.


## Additional Resources

* [Web3JS documentation](https://github.com/ethereum/wiki/wiki/JavaScript-API) - Documentation for web3.js, an API for interacting with Ethereum network
* [Solidity documentation](https://solidity.readthedocs.io) - Documentation for writing Smart Contracts for the Ethereum Virtual machine
* [Truffle documentaion](http://truffleframework.com/docs/) - Documentation for building Ethereum apps using the Truffle framework
* [Ethereum Pet Shop](http://truffleframework.com/tutorials/pet-shop) - A tutorial developed by the Truffle team to write your first Ethereum application
