# zxp-signer

> A simple, lightweight provider for ZXPSignCmd - the tool used to sign Adobe extensions

[![MIT licensed](https://img.shields.io/badge/license-MIT-blue.svg)](https://opensource.org/licenses/MIT)
![Dependencies](https://img.shields.io/librariesio/release/npm/zxp-signer)
[![Coverage Status](https://coveralls.io/repos/github/Trevor-/zxp-signer/badge.svg?branch=master)](https://coveralls.io/github/Trevor-/zxp-signer?branch=master)

## Credits

This is an independent fork of <https://github.com/codearoni/zxp-provider.git> with updated ZXPSignCmd binaries.  
All the hard work was done by <https://github.com/codearoni>

## Installation

```bash
npm install zxp-signer
```

or

```bash
yarn add zxp-signer
```

## Usage

zxp-signer has a simple interface for calling ZXPSignCmd. Most users will want to call zxp-signer with no arguments. This will return the latest version of ZXPSignCmd, for your current running operating system.

```javascript
const zxpSigner = require('zxp-signer');
const zxp = zxpSigner(); // returns the lastest version for the current operation system
```

If you would like to manually choose the version of ZXPSignCmd, an interface is provided for that. Please see CEP-Resources if you're unsure what versions are available. If you would like, zxp-signer also contains an Array of supported versions.

```javascript
const chosenVersion = zxpSigner.supportedVersions[0]; // select the oldest version of ZXPSignCmd
const zxp = zxpSigner({ version: chosenVersion });
```

If you would like to manually select the os, you can do that as well. zxp-signer exposes an object containing all of the supported versions.

```javascript
const win64 = zxpSigner.supportedPlatforms.win64; // manually select windows 64 bit
const zxp = zxpSigner({ os: win64 })
```

## Notes

[CEP-Resources](https://github.com/Adobe-CEP/CEP-Resources)
