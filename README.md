<p align="center"><img src="https://i.ibb.co/n0xQ1RY/logo-transparent.png" height="300"></p>
     
Bitcoin Global is a community-driven open-source project. Find more information on how our project works, and how you can help us grow and benefit from it.
     
- [Joining in](#joining-in)
  - [Running a full node](#running-a-full-node)
  - [Running an Electrum server](#running-an-electrum-server)
  - [Miners and mining pools](#miners-and-mining-pools)
- [Infrastructure details](#infrastructure-details)
- [Development Resources](#development-resources)
- [Community](#community)
    
---

## Joining in

Help Bitcoin Global project grow by joining and extending our network. Running any stack will benefit everyone on the network - improving speed, stability and security. 
Below are some of the ways you can help us.

### Running a full node
```bash
git clone https://github.com/bitcoin-global/global-stack && cd ./global-stack
BTG_VERSION="0.19.2"
node/install-node.sh \
    -v ${BTG_VERSION} \
    -r v${BTG_VERSION} \
    -t ~/binaries \
    -d ~/bitcoin-global
```

### Running an Electrum server
```bash
git clone https://github.com/bitcoin-global/global-stack && cd ./global-stack
nano stack/deploy-electrum.sh   # update parameters
stack/deploy-electrum.sh
```

### Miners and mining pools
Bitcoin Global can be mined via same equipment and protocols used for mining Bitcoin, using **SHA256** PoW algorithm. Our [pool.mainnet.bitcoin-global.io:9223](http://pool.mainnet.bitcoin-global.io:9223) mining pool supports **stratum** protocol and can be joined easily 
by both solo miners and mining pools.     


```bash
# Install dependencies: https://bitcointalk.org/index.php?topic=55038.0
git clone https://github.com/bitcoin-global/global-miner && cd ./global-miner
./autogen.sh
./configure
make

# Mine
./minerd -a sha256d \
    --url stratum+tcp://pool.mainnet.bitcoin-global.io:9223 \
    --userpass ${PUBLIC_USERNAME}:. \     # your unique username
    --coinbase-addr ${PAYOUT_ADDRESS}     # your own Bitcoin Global address, eg "GTanHYuaZyUfSfGkSV1TK52YCky5MSbk2Y"
```
     

## Infrastructure details
Bitcoin Global infrastructure stack is hosted across multiple regions for the sake of availiability, low latency, and decentralization. You can help us by running your own
version of the stack by following the [global-stack](https://github.com/bitcoin-global/global-stack) guidelines.
    
ElectrumX | Explorer
--- | ---
[electrumx.us.mainnet.bitcoin-global.io](http://electrumx.us.mainnet.bitcoin-global.io) | [explorer.us.mainnet.bitcoin-global.io](https://explorer.us.mainnet.bitcoin-global.io)

[electrumx.australia.mainnet.bitcoin-global.io](http://electrumx.australia.mainnet.bitcoin-global.io) | [explorer.australia.mainnet.bitcoin-global.io](https://explorer.australia.mainnet.bitcoin-global.io)
[electrumx.europe.mainnet.bitcoin-global.io](http://electrumx.europe.mainnet.bitcoin-global.io) | [explorer.europe.mainnet.bitcoin-global.io](https://explorer.europe.mainnet.bitcoin-global.io)
    
Main servers are located in Europe, referenced as:
* **Explorer** - [mainnet.bitcoin-global.io](https://mainnet.bitcoin-global.io)
* **ElectrumX** - [electrumx.mainnet.bitcoin-global.io](http://electrumx.mainnet.bitcoin-global.io)
* **Mining pool** - [pool.mainnet.bitcoin-global.io:9223](http://pool.mainnet.bitcoin-global.io:9223)

`Note`: Mainnet and testnet infrastructure references differ by `{mainnet}` and `{testnet}` attributes.

     

## Development Resources

- Bitcoin Global
  - **[bitcoin-global](https://github.com/bitcoin-global/bitcoin-global)** - Bitcoin Global full node and wallet reference implementation.
  - **[global-stack](https://github.com/bitcoin-global/global-stack)** - Best practices on how to run Bitcoin Global community infrastructure stack.
  
- Electrum Global
  - **[electrum-global](https://github.com/bitcoin-global/global-electrum)** - Thin wallet implementation for Bitcoin Global project.
  - **[electrumX](https://github.com/bitcoin-global/global-electrumx)** - Electrum server that supports thin wrapper wallets.

- Lightning Network (*in development*)
  - **[lnd](https://github.com/bitcoin-global/lnd)** - A Go implementation of Lightning Network for Bitcoin Global.
  - **[ln-explorer](https://github.com/bitcoin-global/ln-explorer)** - A Lightning Network explorer web service.

- Tools & Libraries
  - **[explorer](https://github.com/bitcoin-global/explorer/)** Database-free Bitcoin Global blockchain explorer.
  - **[global-seeder](https://github.com/bitcoin-global/global-seeder)** DNS seeder for Bitcoin Global.

- Mining
  - **[global-miner](https://github.com/bitcoin-global/global-miner)** - Multi-threaded  CPU miner for Bitcoin Global.
  - **[global-p2pool](https://github.com/bitcoin-global/global-p2pool)** - Peer-to-peer Bitcoin Global mining pool.

     

## Community


* [Telegram](https://t.me/BitcoinGlobalOffical)
* [Discord](https://discord.gg/JFtQdk9)
* [Twitter](https://twitter.com/bitcoinglobalio)
* [Facebook](https://www.facebook.com/BitcoinGlobalGLOB)
* [Reddit](https://www.reddit.com/user/Bitcoin-Global)

