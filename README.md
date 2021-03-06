# chromanode

[![build status](https://img.shields.io/travis/chromaway/chromanode.svg?branch=master&style=flat-square)](http://travis-ci.org/chromaway/chromanode)
[![js-standard-style](https://img.shields.io/badge/code%20style-standard-brightgreen.svg?style=flat-square)](https://github.com/feross/standard)

*Chromanode* is open source bitcoin blockchain API (http and websocket support) writeen on JavaScript and uses PostgreSQL for storage.

## Requirements

  * [Bitcoin](https://bitcoin.org/en/download) with txindex=1
  * [node.js](http://www.nodejs.org/download/) (testned only with v0.10)
  * [PostgreSQL](http://www.postgresql.org/download/)

## Installation

  Clone repository:

    $ git clone https://github.com/chromaway/chromanode.git && cd chromanode

  Install dependencides:

    $ npm install

  Edit configs:

    $ vim config/master.yml config/slave.yml

  Run master node:

    $ ./bin/chromanode-master.js -c config/master.yml

  Run slave node (only one slave instance supported now):

    $ ./bin/chromanode-slave.js -c config/slave.yml

## API

[API v1](docs/API_v1.md)

To get current version of chromanode make request to `/version`

## Other open source blockchain apis

  * [Insight-api](https://github.com/bitpay/insight-api)
  * [Toshi](https://github.com/coinbase/toshi)
  * [Electrum-server](https://github.com/spesmilo/electrum-server)
  * [MyChain](https://github.com/thofmann/mychain)

## License

Code released under [the MIT license](https://github.com/chromaway/chromanode/blob/master/LICENSE).

## Todo

  * store scriptPubKey? scriptSig?
  * switch to electrumjs table structure
  * implement status method
  * return coins (txid, outputindex, value, script, confirmations|height) in addressesQuery?
  * update config (using default value)
  * romove `soop` package?
  * code refactoring!
  * add tests (regtest mode?)
