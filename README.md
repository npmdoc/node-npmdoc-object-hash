# api documentation for  [object-hash (v1.1.7)](https://github.com/puleos/object-hash)  [![npm package](https://img.shields.io/npm/v/npmdoc-object-hash.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-object-hash) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-object-hash.svg)](https://travis-ci.org/npmdoc/node-npmdoc-object-hash)
#### Generate hashes from javascript objects in node and the browser.

[![NPM](https://nodei.co/npm/object-hash.png?downloads=true)](https://www.npmjs.com/package/object-hash)

[![apidoc](https://npmdoc.github.io/node-npmdoc-object-hash/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-object-hash_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-object-hash/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-object-hash/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-object-hash/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Scott Puleo",
        "email": "puleos@gmail.com"
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
        "shasum": "a8d83fdf5d4583a4e2e7ffc18e8915e08482ef52",
        "tarball": "https://registry.npmjs.org/object-hash/-/object-hash-1.1.7.tgz"
    },
    "engines": {
        "node": ">= 0.10.0"
    },
    "gitHead": "e4061ba0abe0d6a54fc878867439c799f7f42b2c",
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
            "name": "addaleax",
            "email": "anna@addaleax.net"
        },
        {
            "name": "puleos",
            "email": "puleos@gmail.com"
        }
    ],
    "name": "object-hash",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/puleos/object-hash.git"
    },
    "scripts": {
        "prepublish": "gulp dist",
        "test": "node ./node_modules/.bin/mocha test"
    },
    "version": "1.1.7"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module object-hash](#apidoc.module.object-hash)
1.  [function <span class="apidocSignatureSpan">object-hash.</span>MD5 (object)](#apidoc.element.object-hash.MD5)
1.  [function <span class="apidocSignatureSpan">object-hash.</span>keys (object)](#apidoc.element.object-hash.keys)
1.  [function <span class="apidocSignatureSpan">object-hash.</span>keysMD5 (object)](#apidoc.element.object-hash.keysMD5)
1.  [function <span class="apidocSignatureSpan">object-hash.</span>sha1 (object)](#apidoc.element.object-hash.sha1)
1.  [function <span class="apidocSignatureSpan">object-hash.</span>writeToStream (object, options, stream)](#apidoc.element.object-hash.writeToStream)



# <a name="apidoc.module.object-hash"></a>[module object-hash](#apidoc.module.object-hash)

#### <a name="apidoc.element.object-hash.MD5"></a>[function <span class="apidocSignatureSpan">object-hash.</span>MD5 (object)](#apidoc.element.object-hash.MD5)
- description and source-code
```javascript
MD5 = function (object){
  return objectHash(object, {algorithm: 'md5', encoding: 'hex'});
}
```
- example usage
```shell
...
*Sugar method, equivalent to hash(value, {algorithm: 'sha1'})*

## hash.keys(value);
Hash object keys using the sha1 algorithm, values ignored.

*Sugar method, equivalent to hash(value, {excludeValues: true})*

## hash.MD5(value);
Hash using the md5 algorithm.

*Sugar method, equivalent to hash(value, {algorithm: 'md5'})*

## hash.keysMD5(value);
Hash object keys using the md5 algorithm, values ignored.
...
```

#### <a name="apidoc.element.object-hash.keys"></a>[function <span class="apidocSignatureSpan">object-hash.</span>keys (object)](#apidoc.element.object-hash.keys)
- description and source-code
```javascript
keys = function (object){
  return objectHash(object, {excludeValues: true, algorithm: 'sha1', encoding: 'hex'});
}
```
- example usage
```shell
...
    this['_' + objType](object);
  } else if (options.ignoreUnknown) {
    return write('[' + objType + ']');
  } else {
    throw new Error('Unknown object type "' + objType + '"');
  }
}else{
  var keys = Object.keys(object).sort();
  // Make sure to incorporate special properties, so
  // Types with different prototypes will produce
  // a different hash and objects derived from
  // different functions ('new Foo', 'new Bar') will
  // produce different hashes.
  // We never do this for native functions since some
  // seem to break because of that.
...
```

#### <a name="apidoc.element.object-hash.keysMD5"></a>[function <span class="apidocSignatureSpan">object-hash.</span>keysMD5 (object)](#apidoc.element.object-hash.keysMD5)
- description and source-code
```javascript
keysMD5 = function (object){
  return objectHash(object, {algorithm: 'md5', encoding: 'hex', excludeValues: true});
}
```
- example usage
```shell
...
*Sugar method, equivalent to hash(value, {excludeValues: true})*

## hash.MD5(value);
Hash using the md5 algorithm.

*Sugar method, equivalent to hash(value, {algorithm: 'md5'})*

## hash.keysMD5(value);
Hash object keys using the md5 algorithm, values ignored.

*Sugar method, equivalent to hash(value, {algorithm: 'md5', excludeValues: true})*

## hash.writeToStream(value, [options,] stream):
Write the information that would otherwise have been hashed to a stream, e.g.:
'''js
...
```

#### <a name="apidoc.element.object-hash.sha1"></a>[function <span class="apidocSignatureSpan">object-hash.</span>sha1 (object)](#apidoc.element.object-hash.sha1)
- description and source-code
```javascript
sha1 = function (object){
  return objectHash(object);
}
```
- example usage
```shell
...
*  'respectType' {true|false} Whether special type attributes ('.prototype', '.__proto__', '.constructor')
   are hashed. default: true
*  'unorderedArrays' {true|false} Sort all arrays using before hashing. Note that this affects *all* collections,
   i.e. including typed arrays, Sets, Maps, etc. default: false
*  'unorderedSets' {true|false} Sort 'Set' and 'Map' instances before hashing, i.e. make
   'hash(new Set([1, 2])) == hash(new Set([2, 1]))' return 'true'. default: true

## hash.sha1(value);
Hash using the sha1 algorithm.

*Sugar method, equivalent to hash(value, {algorithm: 'sha1'})*

## hash.keys(value);
Hash object keys using the sha1 algorithm, values ignored.
...
```

#### <a name="apidoc.element.object-hash.writeToStream"></a>[function <span class="apidocSignatureSpan">object-hash.</span>writeToStream (object, options, stream)](#apidoc.element.object-hash.writeToStream)
- description and source-code
```javascript
writeToStream = function (object, options, stream) {
  if (typeof stream === 'undefined') {
    stream = options;
    options = {};
  }

  options = applyDefaults(object, options);

  return typeHasher(options, stream).dispatch(object);
}
```
- example usage
```shell
...
*Sugar method, equivalent to hash(value, {algorithm: 'md5'})*

## hash.keysMD5(value);
Hash object keys using the md5 algorithm, values ignored.

*Sugar method, equivalent to hash(value, {algorithm: 'md5', excludeValues: true})*

## hash.writeToStream(value, [options,] stream):
Write the information that would otherwise have been hashed to a stream, e.g.:
'''js
hash.writeToStream({foo: 'bar', a: 42}, {respectType: false}, process.stdout)
// => e.g. 'object:a:number:42foo:string:bar'
'''

## Installation
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
