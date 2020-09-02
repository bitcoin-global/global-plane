<div align="center">
  <img src="https://i.ibb.co/n0xQ1RY/logo-transparent.png" height="200"><br><br>
</div>
<br>

<p align="center">
	<a href="https://t.me/BitcoinGlobalOffical">Telegram</a>&nbsp;&nbsp;&nbsp;
	<a href="https://discord.gg/JFtQdk9">Discord</a>&nbsp;&nbsp;&nbsp;
	<a href="https://twitter.com/bitcoinglobalio">Twitter</a>&nbsp;&nbsp;&nbsp;
	<a href="https://www.facebook.com/BitcoinGlobalGLOB">Facebook</a>&nbsp;&nbsp;&nbsp;
	<a href="https://www.reddit.com/user/Bitcoin-Global">Reddit</a>
</p>

<p align="center">
	<b>Using Bitcoin Global</b>
</p>

## Contents
- [Address](#address)
- [Wallet](#wallet)
- [Full node](#full-node)
- [Mining](#mining)

---

## Address
A Bitcoin Global address, or simply address, is an identifier of 26-35 alphanumeric characters, beginning with `1`, `G` or `glob1` that represents a possible destination for a payment. 
Addresses can be generated at no cost by any user of Bitcoin Global. For example, using [Bitcoin Global client](https://github.com/bitcoin-global/bitcoin-global/releases), 
one can click "New Address" and be assigned an address. It is also possible to get a Bitcoin Global address using an account at an exchange or a wallet service.

There are currently three address formats in use:
* **P2PKH** which begin with the number **1**, eg: `1BvBMSEYstWetqTFn5Au4m4GFg7xJaNVN2`
* **P2SH** type starting with the letter **G**, eg: `GJ98t1WpEZ73CNmQviecrnyiWrnqRhWNLy`
* **Bech32** type starting with prefix **glob1**, eg: `glob1qar0srrr7xfkvy5l643lydnw9re59gtzzwf5mdq`


## Wallet
Bitcoin Global client is the end-user software that facilitates private key generation and security, payment sending on behalf of a private key, and optionally provides:
* Useful information about the state of the network and transactions
* Information related to the private keys under its management
* Syndication of network events to other peer clients

### Supported wallets
* [Electrum Client](https://github.com/bitcoin-global/global-electrum/releases) - [Documentation](https://electrum.readthedocs.io/en/latest/)

## Full node
Full nodes download every block and transaction and check them against Bitcoin Global's consensus rules. Here are examples of consensus rules, though there are many more:

* Blocks may only create a certain number of bitcoins.
* Transactions must have correct signatures for the bitcoins being spent.
* Transactions/blocks must be in the correct data format.
* Within a single block chain, a transaction output cannot be double-spent.

If a transaction or block violates the consensus rules, then it is absolutely rejected, 
even if every other node on the network thinks that it is valid. This is one of the most important characteristics of full nodes: they do what's right no matter what. 

### Getting started
To run a full node, you can download and install [Bitcoin Global client](https://github.com/bitcoin-global/bitcoin-global/releases).     
#### **Requirements:**
* Disk space. 350 GB
* Memory: (RAM) 1 GB
* Download: 500 MB/day (15 GB/month)*
* Upload: 5 GB/day (150 GB/month)
* Operating system: Windows 7/8.x/10, Mac OS X, Linux

## Mining
Mining is the process of adding transaction records to Bitcoin Global's public ledger of past transactions. 
The ledger of past transactions is called the block chain as it is a chain of blocks. The blockchain serves to confirm transactions to the rest of the network as having taken place. Bitcoin Global nodes use the blockchain to distinguish legitimate Bitcoin Global transactions from attempts to re-spend coins that have already been spent elsewhere.    

Mining is intentionally designed to be resource-intensive and difficult so that the number of blocks found each day by miners remains steady. Individual blocks must contain a proof of work to be considered valid. This proof of work is verified by other Bitcoin nodes each time they receive a block. Bitcoin Global uses the hashcash [SHA256](https://en.bitcoin.it/wiki/Proof_of_work) proof-of-work function.

### Mining Bitcoin Global
To start helping Bitcoin Global by joining the mining network, you will need to create mining payout address where you will recieve the reward for finding blocks.
     
#### Creating the wallet
We advise you to create `Legacy` wallet within the latest **[Electrum Global](https://github.com/bitcoin-global/global-electrum/releases)** client, as it is supported by most softwares.
* Install the latest [Electrum Global](https://github.com/bitcoin-global/global-electrum/releases) client
* Create new wallet (`File` > `New`, or skip this step if launching the client for the first time)
* Select **Standard wallet**
* Select **Create a new seed**
* Select **Legacy** seed type
* Finalize the wallet creation
* Show addresses (`View` > `Show Coins`)
* Select any **recieving P2SH address** as your payout address (should start with `G`)

#### Choosing mining pool
Bitcoin Global can be mined via same equipment and protocols used for mining Bitcoin, using **SHA256** PoW algorithm.     
**List of mining pools supporting Bitcoin Global network:**
* [Official Bitcoin Global mining pool](http://pool.mainnet.bitcoin-global.io:9223)
* [Mining-Dutch](https://www.mining-dutch.nl/)
* [Mining-Coins](http://mining-coins.com/)

#### Start mining
*via mining pools*     
Depending on which mining pool you choose, you will need to follow the available guides on how to start mining. Use your **P2SH address** as payout address.

*as a solo miner*      
To start solo mining Bitcoin Global, you will need to install [global-miner](https://github.com/bitcoin-global/global-miner). 
You can follow this [bitcointalk guide](https://bitcointalk.org/index.php?topic=55038.0) on how to install the mining tool. Use your **P2SH address** as payout address, e.g.     
```minerd -a sha256d --url pool.mainnet.bitcoin-global.io:9223 --userpass YOUR_NAME:. --coinbase-addr YOUR_PAYOUT_ADDRESS```


### References:
* [Bitcointalk](bitcointalk.org)
* [Bitcoin Wiki](https://en.bitcoin.it)
* [Electrum](https://electrum.readthedocs.io/en/latest/)
