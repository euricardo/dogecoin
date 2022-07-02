<h1 align="center">
Dogecoin Core [DOGE, Ð]  
<br/><br/>
<img src="https://static.tumblr.com/ppdj5y9/Ae9mxmxtp/300coin.png" alt="Dogecoin" width="300"/>
</h1>

<div align="center">

[![DogecoinBadge](https://img.shields.io/badge/Doge-Coin-yellow.svg)](https://dogecoin.com)
[![MuchWow](https://img.shields.io/badge/Much-Wow-yellow.svg)](https://dogecoin.com)

</div>

Select language: EN | [CN](./README_zh_CN.md)

Dogecoin is a community-driven cryptocurrency that was inspired by a Shiba Inu meme. The Dogecoin Core software allows anyone to operate a node in the Dogecoin blockchain networks and uses the Scrypt hashing method for Proof of Work. It is adapted from Bitcoin Core and other cryptocurrencies.

For information about the default fees used on the Dogecoin network, please
refer to the [fee recommendation](doc/fee-recommendation.md).

**Website:** [dogecoin.com](https://dogecoin.com)

## Usage 💻

To start your journey with Dogecoin Core, see the [installation guide](INSTALL.md) and the [getting started](doc/getting-started.md) tutorial.

The JSON-RPC API provided by Dogecoin Core is self-documenting and can be browsed with `dogecoin-cli help`, while detailed information for each command can be viewed with `dogecoin-cli help <command>`. Alternatively, see the [Bitcoin Core documentation](https://developer.bitcoin.org/reference/rpc/) - which implement a similar protocol - to get a browsable version.

### Such ports

Dogecoin Core by default uses port `22556` for peer-to-peer communication that
is needed to synchronize the "mainnet" blockchain and stay informed of new
transactions and blocks. Additionally, a JSONRPC port can be opened, which
defaults to port `22555` for mainnet nodes. It is strongly recommended to not
expose RPC ports to the public internet.

| Function | mainnet | testnet | regtest |
| :------- | ------: | ------: | ------: |
| P2P      |   22556 |   44556 |   18444 |
| RPC      |   22555 |   44555 |   18332 |

## Ongoing development - Moon plan 🌒

Dogecoin Core is an open source and community driven software. The development
process is open and publicly visible; anyone can see, discuss and work on the
software.

Main development resources:

* [Github Projects](https://github.com/dogecoin/dogecoin/projects) is used to
  follow planned and in-progress work for upcoming releases.
* [Github Discussion](https://github.com/dogecoin/dogecoin/discussions) is used
  to discuss features, planned and unplanned, related to both the development of
  the Dogecoin Core software, the underlying protocols and the DOGE asset.  
* [Dogecoindev subreddit](https://www.reddit.com/r/dogecoindev/)

### Version strategy
Version numbers are following ```major.minor.patch``` semantics.

### Branches
There are 3 types of branches in this repository:

- **master:** Stable, contains the latest version of the latest *major.minor* release.
- **maintenance:** Stable, contains the latest version of previous releases, which are still under active maintenance. Format: ```<version>-maint```
- **development:** Unstable, contains new code for planned releases. Format: ```<version>-dev```

*Master and maintenance branches are exclusively mutable by release. Planned*
*releases will always have a development branch and pull requests should be*
*submitted against those. Maintenance branches are there for **bug fixes only,***
*please submit new features against the development branch with the highest version.*

## Contributing 🤝

If you find a bug or experience issues with this software, please report it
using the [issue system](https://github.com/dogecoin/dogecoin/issues/new?assignees=&labels=bug&template=bug_report.md&title=%5Bbug%5D+).

Please see [the contribution guide](CONTRIBUTING.md) to see how you can
participate in the development of Dogecoin Core. There are often
[topics seeking help](https://github.com/dogecoin/dogecoin/labels/help%20wanted)
where your contributions will have high impact and get very appreciation. wow.

## Communities 🚀🍾

You can join the communities on different social media.
To see what's going on, meet people & discuss, find the lastest meme, learn
about Dogecoin, give or ask for help, to share your project.

Here are some places to visit:

* [Dogecoin subreddit](https://www.reddit.com/r/dogecoin/)
* [Dogeducation subreddit](https://www.reddit.com/r/dogeducation/)
* [Discord](https://discord.gg/dogecoin)
* [Dogecoin Twitter](https://twitter.com/dogecoin)

## License - Much license ⚖️
Dogecoin Core is released under the terms of the MIT license. See
[COPYING](COPYING) for more information or see
[opensource.org](https://opensource.org/licenses/MIT)

## Very Much Frequently Asked Questions ❓

Do you have a question regarding Dogecoin? An answer is perhaps already in the
[FAQ](doc/FAQ.md) or the
[Q&A section](https://github.com/dogecoin/dogecoin/discussions/categories/q-a)
of the discussion board!

Instalação ( passo a passo ) | Todas as etapas de implantação

# apt-get update

apt-get install libboost-all-dev libzmq3-dev libminiupnpc-dev

apt-get install curl git build-essential libtool autotools-dev

apt-get install automake pkg-config bsdmainutils python3

apt-get install software-properties-common libssl-dev libevent-dev

# Clone the repo
git clone https://github.com/euricardo/dogecoin.git

# Pick the correct branch/version
cd dogecoin
git checkout 1.14-branding

# Install dependencies
sudo apt install build-essential libtool autotools-dev autoconf pkg-config libssl-dev

# Autogen
./autogen.sh

# Configure
./configure

# If this error https://github.com/dogecoin/dogecoin/issues/1497
sudo apt-get install libboost-all-dev libdb5.3-dev libdb5.3++-dev libevent-dev

# Then try again with the "--with-incompatible-bdb" because by default dogecoin want 5.1 but it is not available in 18.04
./configure --with-incompatible-bdb

# Make
make

# Build
make install
