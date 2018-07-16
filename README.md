# Gekko [![npm](https://img.shields.io/npm/dm/gekko.svg)]() [![Build Status](https://travis-ci.org/askmike/gekko.png)](https://travis-ci.org/askmike/gekko) [![Build status](https://ci.appveyor.com/api/projects/status/github/askmike/gekko?branch=stable&svg=true)](https://ci.appveyor.com/project/askmike/gekko)

Crypto Trading Bot based on askmike/gekko v0.6.x

- Use postgresql DB as default db to prevent sqlite lock scenarios
  - Rewritten postgres plugin, using connection pooling and transaction safe candle writing (Postgres 9.5+ required)
- HitBtc exchange support based on v2 API and ccxt library (working with Gekko v0.6.x)
  - Market watcher
  - History import
  - Live trading
- HuobiPro exchange support
  - Market watcher
  - Live trading
- OKEX exchange support
  - Market watcher
  - Live trading
- Extended log output
  - mailer.js informs with buy and sell events by mail (different to go short/long advices)
  - More info during paper trader backtesting
- Added often used package dependencies by default to get started quickly (npm install)

## Getting started

- git clone https://github.com/mark-sch/gekko
- cd gekko
- npm install
- cd exchange
- npm install
- cd ..
- npm start

from time to time the exchange markets should be updated with a utility - to get new coin pairs:

- cd exchange/util/genMarketFiles/
- node update-kraken.js
- node update-binance.js

(postgresql experience required to previously setup postgres. Sample config assumes an existing db user gekkodbuser, pass 1234, with added role permission to createdb. PostgreSQL 9.5+ required.)

## Documentation

See [the documentation website](https://gekko.wizb.it/docs/introduction/about_gekko.html).

## Installation & Usage

See [the installing Gekko doc](https://gekko.wizb.it/docs/installation/installing_gekko.html).

## Community & Support

Gekko has [a forum](https://forum.gekko.wizb.it/) that is the place for discussions on using Gekko, automated trading and exchanges. In case you rather want to chat in realtime about Gekko feel free to join the [Gekko Support Discord](https://discord.gg/26wMygt).

## Final

If Gekko helped you in any way, you can always leave me a tip at (BTC) 13r1jyivitShUiv9FJvjLH7Nh1ZZptumwW
