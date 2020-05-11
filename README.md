# Agoric Auction Dapp

The Auction Dapp is a simple [Agoric
Dapp. It simulates an auction platform using the Zoe Smart Contract it has:
1. the browser UI (the frontend)
2. the API server (the backend)
3. the on-chain contract

This dapp starts a local
blockchain on your computer, and deploys a basic contract to that
blockchain. It does not currently deploy or connect to the Agoric testnet.

This particular dapp UI is written in vanilla JS and styled using CSS3.

## Functionality

The Auction Dapp:

1. Subscribes to contract notifications via the API server
2. Accesses your Agoric wallet, and
3. At the user's request:

    1. Can make a BID on an ASSET
    2. proposes (via the user's wallet and Zoe) exchanging a BID for
       ASSET if it meets the ASSET owner requirements.

## Running It Locally

[Ensure you already have Agoric Setup using this guide](https://agoric.com/documentation/getting-started/before-using-agoric.html)


Open a terminal and clone the repo to your local machine and install the dependencies by doing the following:

```bash
git clone https://github.com/emmaodia/agoric-auction-dapp.git
cd agoric-auction-dapp
cd demo
agoric install
agoric start --reset
```
Leave the terminal running and open another terminal where you will run the following commands

```bash
cd agoric-auction-dapp
cd demo
agoric deploy ./contract/deploy.js ./api/deploy.js
cd ui
yarn install
```
Start the application in a development environment via:

```bash
yarn start
```
Application will be running on ```http://localhost:3000```

Go to another tab or browser and open ```http://localhost:8000/``` to see and interact with a basic wallet and a REPL

## Stack

* [Agoric SDK](https://github.com/Agoric/agoric-sdk) - monorepo for the Agoric Javascript smart contract platform.
* [Zoe](https://agoric.com/documentation/zoe/guide/) - Zoe smart contracts are written in the familiar language of JavaScript.

## Credits
I'm grateful to: <br/> The Agoric Team <br/> Gitcoin <br/> Google <br/> Stack Overflow <br/> MDN <br/> 

## Author
Emmanuel Oaikhenan

## License
Apache-2.0. copyright 2020