# Metalsmith Assets Convention Plugin [![NPM version](https://img.shields.io/npm/v/metalsmith-assets-convention.svg)](https://www.npmjs.org/package/metalsmith-assets-convention)

[![Build Status](https://img.shields.io/travis/RobLoach/metalsmith-assets-convention/master.svg)](https://travis-ci.org/RobLoach/metalsmith-assets-convention)
[![Dependency Status](https://david-dm.org/RobLoach/metalsmith-assets-convention.png)](https://david-dm.org/RobLoach/metalsmith-assets-convention)

[Metalsmith](http://metalsmith.io) plugin to define [static asset files](https://github.com/treygriffith/metalsmith-assets) through file conventions.

## Installation

    npm install --save metalsmith-assets-convention

### CLI

If you are using the command-line version of Metalsmith, you can install via npm, and then add the `metalsmith-assets-convention` key to your `metalsmith.json` file:

```json
{
  "plugins": {
    "metalsmith-assets-convention": {
      "extname": ".assets"
    }
  }
}
```

### JavaScript

If you are using the JS Api for Metalsmith, then you can require the module and add it to your `.use()` directives:

```js
var assets = require('metalsmith-assets-convention');

metalsmith.use(assets({
  extname: '.assets'
}));
```

## Usage

Each static file copy is handled through naming the `<name>.assets` files. The file's metadata options are passed off to [`metalsmith-assets`](https://github.com/treygriffith/metalsmith-assets) to copy the assets. All [`metalsmith-assets` options](https://github.com/treygriffith/metalsmith-assets#using-the-cli) apply, defined through each .static file:

### Example
#### `src/public.static`
``` yaml
---
source: public
destination: .
---
Copy all the public files into the built directory.
```

## License

MIT