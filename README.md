Litecore Node
============

[![NPM Package](https://img.shields.io/npm/v/litecore-node.svg?style=flat-square)](https://www.npmjs.org/package/litecore-node)
[![Build Status](https://img.shields.io/travis/litecoin-project/litecore-node.svg?branch=master&style=flat-square)](https://travis-ci.org/litecoin-project/litecore-node)
[![Coverage Status](https://img.shields.io/coveralls/litecoin-project/litecore-node.svg?style=flat-square)](https://coveralls.io/r/litecoin-project/litecore-node)

A Litecoin full node for building applications and services with Node.js. A node is extensible and can be configured to run additional services. At the minimum a node has an interface to [Litecoin Core with additional indexing](https://github.com/litecoin-project/litecore-litecoin) for more advanced address queries. Additional services can be enabled to make a node more useful such as exposing new APIs, running a block explorer and wallet service.

## Install

```bash
npm install -g litecore-node
litecore-node start
```

Note: For your convenience, we distribute litecoind binaries for x86_64 Linux and x86_64 Mac OS X. Upon npm install, the binaries for your platform will be downloaded. For more detailed installation instructions, or if you want to compile the project yourself, then please see the Litecore branch of [Litecoin Core with additional indexing](https://github.com/litecoin-project/litecore-litecoin).

## Prerequisites

- GNU/Linux x86_32/x86_64, or OSX 64bit *(for litecoind distributed binaries)*
- Node.js v8.11.4 (LTS)
- ZeroMQ *(libzmq3-dev for Ubuntu/Debian or zeromq on OSX)*
- ~200GB of disk storage
- ~8GB of RAM

## Configuration

Litecore includes a Command Line Interface (CLI) for managing, configuring and interfacing with your Litecore Node.

```bash
litecore-node create -d <litecoin-data-dir> mynode
cd mynode
litecore-node install <service>
litecore-node install https://github.com/yourname/helloworld
```

This will create a directory with configuration files for your node and install the necessary dependencies. For more information about (and developing) services, please see the [Service Documentation](docs/services.md).

## Add-on Services

There are several add-on services available to extend the functionality of Litecore:

- [Insight Lite API](https://github.com/litecoin-project/insight-lite-api)
- [Insight Lite UI](https://github.com/litecoin-project/insight-lite-ui)
- [Litecore Wallet Service](https://github.com/litecoin-project/litecore-wallet-service)

## Documentation

- [Upgrade Notes](docs/upgrade.md)
- [Services](docs/services.md)
  - [Bitcoind](docs/services/bitcoind.md) - Interface to Litecoin Core
  - [Web](docs/services/web.md) - Creates an express application over which services can expose their web/API content
- [Development Environment](docs/development.md) - Guide for setting up a development environment
- [Node](docs/node.md) - Details on the node constructor
- [Bus](docs/bus.md) - Overview of the event bus constructor
- [Release Process](docs/release.md) - Information about verifying a release and the release process.

## Contributing

Please send pull requests for bug fixes, code optimization, and ideas for improvement. For more information on how to contribute, please refer to our [CONTRIBUTING](https://github.com/litecoin-project/litecore/blob/master/CONTRIBUTING.md) file.

## License

Code released under [the MIT license](https://github.com/litecoin-project/litecore-node/blob/master/LICENSE).

Copyright 2018 The Litecoin Core Developers

- bitcore: Copyright (c) 2013-2015 BitPay, Inc. (MIT License)
- bitcoin: Copyright (c) 2009-2015 Bitcoin Core Developers (MIT License)
