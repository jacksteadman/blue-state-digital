# blue-state-digital

[![Generated with nod](https://img.shields.io/badge/generator-nod-2196F3.svg?style=flat-square)](https://github.com/diegohaz/nod)
[![NPM version](https://img.shields.io/npm/v/blue-state-digital.svg?style=flat-square)](https://npmjs.org/package/blue-state-digital)
[![Build Status](https://img.shields.io/travis/robertsonsamuel/blue-state-digital/master.svg?style=flat-square)](https://travis-ci.org/robertsonsamuel/blue-state-digital) [![Coverage Status](https://img.shields.io/codecov/c/github/robertsonsamuel/blue-state-digital/master.svg?style=flat-square)](https://codecov.io/gh/robertsonsamuel/blue-state-digital/branch/master)

A node module for accessing the blue state digital api service

## Install

    $ npm install --save blue-state-digital

## Usage

```js
import myModule from 'blue-state-digital'

myModule()
```

## API

<!-- Generated by documentation.js. Update this documentation by updating the source code. -->

### BSD

Create a new BSD rest client.

**Parameters**

-   `options` **[object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)** The BSD API Options.
    -   `options.baseUrl` **[String](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** The base url of your bsd instance. IE: <https://XYZ>
    -   `options.apiID` **[String](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** The App ID for your BSD API Secret.
    -   `options.apiSecret` **[String](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** The API Secret for your BSD API App.
    -   `options.apiVer` **[Number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)** The API version, default is 2 and 2 is only supported for now.

**Examples**

_The <b>BSD</b> constructor takes a API
  ID, if specified it will be used as default value for all endpoints that
  accept a API ID. The default is 2 but is required
  so you are aware of what version you are using._

```javascript
const blueStateDigital = new BSD({
  baseUrl: 'legislator.bsd.net',
  apiID: 'MyApiID',
  apiSecret: '43875utihgkfj38563y4uig',
  apiVer: 2,
})
```

### utils

## License

MIT © [Samuel Robertson](https://www.robertsonsamuel.com)
