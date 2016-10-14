# CSS Asset Copier #

## Features ##

- Designed to be used with `css-url-rewriter-ex` library
- Copy CSS related local assets to target directory
- Covered by unit tests

## Installation ##

```shell
npm install css-asset-copier
```

## Usage ##

```javascript
var CssUrlRewriter = require('css-url-rewriter-ex');
var CssAssetCopier = require('css-asset-copier');

const rewriter = new CssUrlRewriter();
const assetCopier = new CssAssetCopier('dist');

rewriter.rewrite(filename, content);

assetCopier.copyAssets(rewriter.getLocalAssetList())
  .then(() => {
    console.log('Done!');
  });
```
