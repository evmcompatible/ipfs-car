# Changelog

## 1.0.0 (2022-08-28)


### ⚠ BREAKING CHANGES

* iana media type application/vnd.ipld.car (#119)
* packToBlob function returns new @web-std/blob
* We rely now on an extended version of the new ipfs blockstore interface to be compatible with the new ipfs-unixfs. Previously unixfs was using a simple block API from ipld which returned blocks everywhere, while now put returns a void Promise and get returns the bytes instead of the Block. Destroy was also renamed to close to be the same as the interface. The only addition in the interface is the blocks async iterator function. All the blocktore implementations extend BlockstoreAdapter to have all the API expected by the interface.

### Features

* add option to disable wrapping with directory in cli ([#101](https://github.com/evmcompatible/ipfs-car/issues/101)) ([65a32d4](https://github.com/evmcompatible/ipfs-car/commit/65a32d4e3ac40c438dacfbfbc0ef1d9cc77e8543))
* add pipe car in from stdin ([#2](https://github.com/evmcompatible/ipfs-car/issues/2)) ([a4c80bc](https://github.com/evmcompatible/ipfs-car/commit/a4c80bcc39a99861382324164822d217872792c3))
* add rawLeaves option to allow for downgradable CID ([#105](https://github.com/evmcompatible/ipfs-car/issues/105)) ([88940df](https://github.com/evmcompatible/ipfs-car/commit/88940dfe39378b9a666f317ec37a89047395b36f))
* add unpackStream ([#46](https://github.com/evmcompatible/ipfs-car/issues/46)) ([e5d72f1](https://github.com/evmcompatible/ipfs-car/commit/e5d72f1a5a6cf459484e6639b097fa74d2e63931))
* blockstore ([#11](https://github.com/evmcompatible/ipfs-car/issues/11)) ([d122b2a](https://github.com/evmcompatible/ipfs-car/commit/d122b2a670cc328522524d4e15f8a58d72cc98f6))
* display cids with associated filename ([#124](https://github.com/evmcompatible/ipfs-car/issues/124)) ([9ebb328](https://github.com/evmcompatible/ipfs-car/commit/9ebb328b3d15cf4691a53d74516c197d908d5aa0))
* from car ([5b3ffbd](https://github.com/evmcompatible/ipfs-car/commit/5b3ffbd4c29a2f30b24c2f7961f980dd39094ee7))
* from car ([5b3ffbd](https://github.com/evmcompatible/ipfs-car/commit/5b3ffbd4c29a2f30b24c2f7961f980dd39094ee7))
* from car ([8667da4](https://github.com/evmcompatible/ipfs-car/commit/8667da4ed28d313dd5432b9af6255bdaed796a31))
* iana media type application/vnd.ipld.car ([#119](https://github.com/evmcompatible/ipfs-car/issues/119)) ([739c00d](https://github.com/evmcompatible/ipfs-car/commit/739c00d44def41441757911e61c0d2869eef7d1d))
* idb blockstore ([#45](https://github.com/evmcompatible/ipfs-car/issues/45)) ([966f1ba](https://github.com/evmcompatible/ipfs-car/commit/966f1ba09788abc6ac87a9bbf6b6c995a5f6ea0b))
* implement has ([#95](https://github.com/evmcompatible/ipfs-car/issues/95)) ([82b566c](https://github.com/evmcompatible/ipfs-car/commit/82b566c54b8c687040c6c577fac138a60ceb7839))
* nice cli for --pack and --unpack ([686632c](https://github.com/evmcompatible/ipfs-car/commit/686632c4430c0a1b1429f4b228fa5b0668b7f658))
* pack cli output with filename and root ([#13](https://github.com/evmcompatible/ipfs-car/issues/13)) ([254c4e8](https://github.com/evmcompatible/ipfs-car/commit/254c4e8a88c1523b14119ad007aca6cadd667c1f))
* pack supports custom unixfs importer options ([#61](https://github.com/evmcompatible/ipfs-car/issues/61)) ([44372e7](https://github.com/evmcompatible/ipfs-car/commit/44372e707b531aa37fec80c1b6411c53e15e2a7d))
* release workflow ([#128](https://github.com/evmcompatible/ipfs-car/issues/128)) ([6fffa74](https://github.com/evmcompatible/ipfs-car/commit/6fffa74df82cdc08ba9588b381db4d75db462ca3))
* support custom max children per node ([#67](https://github.com/evmcompatible/ipfs-car/issues/67)) ([2b7fe86](https://github.com/evmcompatible/ipfs-car/commit/2b7fe8629a2fb7bc1e317e5453db324b81f0b131))
* toCar ([#4](https://github.com/evmcompatible/ipfs-car/issues/4)) ([c48f646](https://github.com/evmcompatible/ipfs-car/commit/c48f646da7f092f48ff9176c2dac07634586351c))
* unpack 1 or more roots from a car ([#3](https://github.com/evmcompatible/ipfs-car/issues/3)) ([3a8d422](https://github.com/evmcompatible/ipfs-car/commit/3a8d422d9eb80696bed25801d29edfc040a0fa58))


### Bug Fixes

* add js extension to normalize input in stream ([#38](https://github.com/evmcompatible/ipfs-car/issues/38)) ([d71f496](https://github.com/evmcompatible/ipfs-car/commit/d71f4962c602bd54f291e84ecb5ca30025a30a50))
* add package json to esm build to hint module ([#33](https://github.com/evmcompatible/ipfs-car/issues/33)) ([584676a](https://github.com/evmcompatible/ipfs-car/commit/584676a477796773057876db6ad6e180b29e9f3d))
* always wrap in directory on pack ([#57](https://github.com/evmcompatible/ipfs-car/issues/57)) ([9bf1378](https://github.com/evmcompatible/ipfs-car/commit/9bf13783b25d92c093ebcc076cb7c47810c58f12))
* async CAR put() & close() for backpressure & error handling ([#74](https://github.com/evmcompatible/ipfs-car/issues/74)) ([42d5dde](https://github.com/evmcompatible/ipfs-car/commit/42d5dde40d2d65f1bffa18432f741088a380c065))
* do not use uin8array default export ([#43](https://github.com/evmcompatible/ipfs-car/issues/43)) ([f01ea25](https://github.com/evmcompatible/ipfs-car/commit/f01ea2567053bb11c1f6995bd714a97f428836d8))
* empty input array ([#59](https://github.com/evmcompatible/ipfs-car/issues/59)) ([b0c0570](https://github.com/evmcompatible/ipfs-car/commit/b0c0570e9a36c237797b2a7dcc6628420b027fc5))
* esm imports need js extension ([#34](https://github.com/evmcompatible/ipfs-car/issues/34)) ([5043bb5](https://github.com/evmcompatible/ipfs-car/commit/5043bb590b92bb6191c5dfc3f67a691642d30a94))
* exports in ts ([#18](https://github.com/evmcompatible/ipfs-car/issues/18)) ([892111c](https://github.com/evmcompatible/ipfs-car/commit/892111cfb1039a74dfe994303e1e9f8f6665d677))
* file extension typo ([#23](https://github.com/evmcompatible/ipfs-car/issues/23)) ([5436bf0](https://github.com/evmcompatible/ipfs-car/commit/5436bf0f257ee6ecbfbe54610739709c20d55f4b))
* fs blockstore destroy without open ([#49](https://github.com/evmcompatible/ipfs-car/issues/49)) ([d6e3e47](https://github.com/evmcompatible/ipfs-car/commit/d6e3e4789a35697076bfe976ff33b6e3bf1a0355))
* fs blockstore race condition ([#16](https://github.com/evmcompatible/ipfs-car/issues/16)) ([35d4b30](https://github.com/evmcompatible/ipfs-car/commit/35d4b30adc3d726ebb7231b196ad5dd112d5ad3d))
* import stream to it ([#52](https://github.com/evmcompatible/ipfs-car/issues/52)) ([4a79d03](https://github.com/evmcompatible/ipfs-car/commit/4a79d031fbd4de2984e50d4a2a52b792bd5d2e9b))
* memory blockstore types ([#54](https://github.com/evmcompatible/ipfs-car/issues/54)) ([6ffd5f8](https://github.com/evmcompatible/ipfs-car/commit/6ffd5f897cd7e55b941c52e7deb9f91249838f22))
* move sinon types dep to devDeps ([#28](https://github.com/evmcompatible/ipfs-car/issues/28)) ([8daa4b5](https://github.com/evmcompatible/ipfs-car/commit/8daa4b5a8f6ddb353f457937aebafc9f3c724ba4))
* race condition using pack to blob ([#85](https://github.com/evmcompatible/ipfs-car/issues/85)) ([54175d0](https://github.com/evmcompatible/ipfs-car/commit/54175d01b1bbbf88d896d436d0b3911c1d39f015))
* readme contributing and license ([e4cf245](https://github.com/evmcompatible/ipfs-car/commit/e4cf245923407fdd44b1ddf8426248a4393e4cc6))
* show the full filename in output for --pack ([#22](https://github.com/evmcompatible/ipfs-car/issues/22)) ([3842f99](https://github.com/evmcompatible/ipfs-car/commit/3842f9985a8d16018290205bf8fdabf6bc5de4fb))
* use exporter with types ([#6](https://github.com/evmcompatible/ipfs-car/issues/6)) ([9ffece6](https://github.com/evmcompatible/ipfs-car/commit/9ffece696fb64ea0b2cf31146bf843bb3831e39f))
* use web-std blob ([#25](https://github.com/evmcompatible/ipfs-car/issues/25)) ([e16683f](https://github.com/evmcompatible/ipfs-car/commit/e16683f4df97cc7633b0ef4c24e2805475e74cdc))


### Miscellaneous Chores

* update dependencies ([#103](https://github.com/evmcompatible/ipfs-car/issues/103)) ([df41901](https://github.com/evmcompatible/ipfs-car/commit/df41901eff484583f171399dc425a63ff225765a))
* use ipfs-unixfs final release instead of fork ([#56](https://github.com/evmcompatible/ipfs-car/issues/56)) ([21b3791](https://github.com/evmcompatible/ipfs-car/commit/21b37910afe26e88b26b2fc86d693c02801aa787))

## [0.8.1](https://github.com/web3-storage/ipfs-car/compare/v0.8.0...v0.8.1) (2022-08-05)


### Bug Fixes

* readme contributing and license ([e4cf245](https://github.com/web3-storage/ipfs-car/commit/e4cf245923407fdd44b1ddf8426248a4393e4cc6))

## [0.8.0](https://github.com/web3-storage/ipfs-car/compare/v0.7.0...v0.8.0) (2022-08-02)


### Features

* display cids with associated filename ([#124](https://github.com/web3-storage/ipfs-car/issues/124)) ([9ebb328](https://github.com/web3-storage/ipfs-car/commit/9ebb328b3d15cf4691a53d74516c197d908d5aa0))
* release workflow ([#128](https://github.com/web3-storage/ipfs-car/issues/128)) ([6fffa74](https://github.com/web3-storage/ipfs-car/commit/6fffa74df82cdc08ba9588b381db4d75db462ca3))
