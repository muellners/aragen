# AraGen [![Build Status](https://travis-ci.org/aragon/aragen.svg?branch=master)](https://travis-ci.org/aragon/aragen) [![npm](https://img.shields.io/npm/v/@aragon/aragen.svg?style=for-the-badge)](https://www.npmjs.com/package/@aragon/aragen)

Generate an Aragon environment

### Requirements

- `npm`
- `git`

### How to

```
npm i
npm run gen
npm start
```

Yes, you are done. Happy hacking 🔥🦅!

If you happen to stop ganache, just:

```
npm run start-ganache
```

### Using snapshots

The Aragen package published to NPM contains a ganache snapshot that can be used to quickly start a chain with the entire Aragon system ready.

By default it has set up:

- ENS: `0x5f6f7e8cc7346a11ca2def8f827b7a0b612c56a1`
- DAO_FACTORY: `0x5d94e3e7aec542ab0f9129b9a7badeb5b3ca0f77`
- MINIME_FACTORY: `0xd526b7aba39cccf76422835e7fd5327b98ad73c9`
- FIFResolvingRegistrar: `0xf1f8aac64036cdd399886b1c157b7e3b361093f3`

* APM: `ens.addr('aragonpm.eth')`
* AragonID: `ens.owner('aragonid.eth')`
* Aragon apps: As APM repos, e.g. `apm.getLatest('voting.aragonpm.eth')`
* Templates: As APM repos, e.g. `apm.getLatest('democracy-template.aragonpm.eth')`

Use these for Avalanche Fuji testnet:

- ENS On Fuji : `0x5b442a5e9020a886354c77e4ad10b11ddd883714`
- DAOFActory on Fuji : `0x162a99aef64fe71f135f866348910e9df1ac6e1b`
- APM on Fuji: `0xa28f79175244914ae56594531c1a9d213b5f6e98`
- FifsResolverRegistrar: `0xb6dcee47659aef83a6dfa620590b7c07ec6c1264`
 
* AragonID on Fuji: `0xb6dcee47659aef83a6dfa620590b7c07ec6c1264`

To use directly with ganache-cli:

```
npm install @aragon/aragen
npx aragen start
```

If you wish to access from code, for example to run ganache-core directly:

```js
const aragonSnapshot = path.resolve(
  require.resolve("@aragon/aragen"),
  "../aragon-ganache"
);
```

### CI

If you need to trigger the CI so a new snapshot is generated and publish to NPM, you need to tag the release by bumping the NPM version and commit to master.

```
npm version [major, minor, patch]
```

## Getting help

If you need help, please reach out to Aragon core contributors and community members on [Spectrum](https://spectrum.chat/aragon/app-development). We'd love to hear from you and know what you're working on!
