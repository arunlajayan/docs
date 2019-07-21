# Ethereum Truffle

Configure [Truffle Suite](https://truffleframework.com) to deploy contracts to your Ethereum nodes.

1. Install [Truffle Suite](https://truffleframework.com), [HD Wallet-enabled Web3 provider](https://github.com/trufflesuite/truffle-hdwallet-provider), and create a project.

2. Create a new environment in `truffle-config.js`, add your mnemonic phrase generated by [a wallet](https://docs.ethhub.io/using-ethereum/wallets/intro-to-ethereum-wallets/) and the node RPC endpoint:

``` js
const HDWalletProvider = require('truffle-hdwallet-provider');
const mnemonic = 'pattern enroll upgrade ...';
...
module.exports = {
 networks: {
    chainstack: {
        provider: () => new HDWalletProvider(mnemonic, "https://nd-123-456-789.p2pify.com:8545"),
        network_id: 1
    },
   }
  }
};
```

3. Run `truffle migrate --network chainstack` and Truffle will deploy using Chainstack.

::: tip See also
* [Academic certificates on Ethereum](/developer-materials/tutorials/academic-certificates-on-ethereum)
* [Ethereum Embark](/developer-materials/development-tools/ethereum-embark)
:::