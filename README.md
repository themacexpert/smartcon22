# Building Connected Contracts
![Banner Image](https://i.ibb.co/bJ3xhm3/20220926-Chainlink-Smart-Con-Workshop-EXTERNAL.png)
Workshop for Chainlink Smartcon 2022. This guide contains all the links you'll need for the workshop. 

## Send a message to another chain with Axelar
In this demo, we will use Axelar's General message passing to call a contract on another chain. We will be mostly following the steps of [this blog post guide](https://moonbeam.network/blog/connected-contracts-axelar/), with the exception of the **gas amounts**, which have changed since the publish date. 

The required chain names and contract addresses can be found [here on Axelar Docs Site](https://docs.axelar.dev/dev/build/contract-addresses/testnet).

To get started, first copy and paste the contents of [SimpleGeneralMessage.sol](https://gist.github.com/jboetticher/0188244031df80e9b180568e30bfa7a5) into Remix.

The required gas amounts in WEI to send along with the message from Moonbase Alpha are the following: 
- Polygon Mumbai: 339003286300000000
- Avalanche Fuji: 970363238301000000
- Fantom Testnet: 553898649000000000
- Ethereum Ropst: 16000000000000000000
