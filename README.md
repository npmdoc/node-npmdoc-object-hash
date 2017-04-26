# npmdoc-object-hash

#### basic api documentation for  [object-hash (v1.1.8)](https://github.com/puleos/object-hash)  [![npm package](https://img.shields.io/npm/v/npmdoc-object-hash.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-object-hash) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-object-hash.svg)](https://travis-ci.org/npmdoc/node-npmdoc-object-hash)

#### Generate hashes from javascript objects in node and the browser.

[![NPM](https://nodei.co/npm/object-hash.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/object-hash)

- [https://npmdoc.github.io/node-npmdoc-object-hash/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-object-hash/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-object-hash/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-object-hash/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-object-hash/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-object-hash/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Scott Puleo"
    },
    "browser": "./dist/object_hash.js",
    "bugs": {
        "url": "https://github.com/puleos/object-hash/issues"
    },
    "dependencies": {},
    "description": "Generate hashes from javascript objects in node and the browser.",
    "devDependencies": {
        "browserify": "^13.0.0",
        "gulp": "^3.9.0",
        "gulp-browserify": "^0.5.1",
        "gulp-coveralls": "^0.1.4",
        "gulp-exec": "^2.1.2",
        "gulp-istanbul": "^0.10.3",
        "gulp-jshint": "^2.0.0",
        "gulp-mocha": "^2.2.0",
        "gulp-rename": "^1.2.0",
        "gulp-uglify": "^1.5.1",
        "jshint": "^2.8.0",
        "jshint-stylish": "^2.1.0",
        "karma": "^0.13.15",
        "karma-chrome-launcher": "^0.2.2",
        "karma-firefox-launcher": "^0.1.7",
        "karma-mocha": "^0.2.1",
        "karma-phantomjs-launcher": "^0.2.1",
        "mocha": "^2.3.4",
        "phantomjs": "^1.9.19"
    },
    "directories": {},
    "dist": {
        "shasum": "28a659cf987d96a4dabe7860289f3b5326c4a03c",
        "tarball": "https://registry.npmjs.org/object-hash/-/object-hash-1.1.8.tgz"
    },
    "engines": {
        "node": ">= 0.10.0"
    },
    "gitHead": "469439a30fdd41e2f35f2a6aeddebb6a8d923f75",
    "homepage": "https://github.com/puleos/object-hash",
    "keywords": [
        "object",
        "hash",
        "sha1",
        "md5"
    ],
    "license": "MIT",
    "main": "./index.js",
    "maintainers": [
        {
            "name": "addaleax"
        },
        {
            "name": "puleos"
        }
    ],
    "name": "object-hash",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/puleos/object-hash.git"
    },
    "scripts": {
        "prepublish": "gulp dist",
        "test": "node ./node_modules/.bin/mocha test"
    },
    "version": "1.1.8",
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
