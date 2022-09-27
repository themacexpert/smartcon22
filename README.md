# Building Connected Contracts
![Banner Image](https://i.ibb.co/bJ3xhm3/20220926-Chainlink-Smart-Con-Workshop-EXTERNAL.png)
Workshop for Chainlink Smartcon 2022. This guide contains all the links you'll need for the workshop. 

## Send a message to another chain with Axelar
In this demo, we will use Axelar's General message passing to call a contract on another chain. We will be mostly following the steps of [this blog post guide](https://moonbeam.network/blog/connected-contracts-axelar/), with the exception of the **gas amounts**, which have changed since the publish date. 

## Pre-Requisites
- [Faucet for Moonbase Alpha DEV Funds](https://apps.moonbeam.network/moonbase-alpha/faucet/)
- [Add the Moonbase Alpha Network to MetaMask](https://docs.moonbeam.network/)
- [Faucet for Avax Testnet Funds](https://faucet.avax.network/)
- [Add the Avax Fuji Testnet to MetaMask](https://chainlist.org/)

## Building the Contract
You'll need to import the following: 
* import {IAxelarExecutable} from "https://github.com/axelarnetwork/axelar-cgp-solidity/blob/main/contracts/interfaces/IAxelarExecutable.sol";
* import {IAxelarGasService} from "https://github.com/axelarnetwork/axelar-cgp-solidity/blob/main/contracts/interfaces/IAxelarGasService.sol";


The required chain names and contract addresses for the gas services and gateway contracts can be found [here on Axelar Docs Site](https://docs.axelar.dev/dev/build/contract-addresses/testnet).



The required gas amounts in WEI to send along with the message from Moonbase Alpha are the following: 
- Polygon Mumbai: 339003286300000000
- Avalanche Fuji: 970363238301000000
- Fantom Testnet: 553898649000000000
- Ethereum Ropst: 16000000000000000000


### Checking Cross-Chain Transaction Status
First, look up the hash of your txn on the origin chain - in this case, [on the Moonbase Alpha Testnet](https://moonbase.moonscan.io/). Then, lookup that hash on [testnet.axelarscan.io](https://testnet.axelarscan.io/). 

### Need help?
- If you get stuck, you can refer to this sample contract here and/or you can copy and paste the contents of [SimpleGeneralMessage.sol](https://gist.github.com/jboetticher/0188244031df80e9b180568e30bfa7a5) into Remix.
- [Backup Development Accounts Pre-Funded with Testnet Tokens](https://docs.moonbeam.network/builders/get-started/networks/moonbeam-dev/#pre-funded-development-accounts)
