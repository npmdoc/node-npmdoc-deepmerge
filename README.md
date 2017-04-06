# api documentation for  [deepmerge (v1.3.2)](https://github.com/KyleAMathews/deepmerge)  [![npm package](https://img.shields.io/npm/v/npmdoc-deepmerge.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-deepmerge) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-deepmerge.svg)](https://travis-ci.org/npmdoc/node-npmdoc-deepmerge)
#### A library for deep (recursive) merging of Javascript objects

[![NPM](https://nodei.co/npm/deepmerge.png?downloads=true)](https://www.npmjs.com/package/deepmerge)

[![apidoc](https://npmdoc.github.io/node-npmdoc-deepmerge/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-deepmerge_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-deepmerge/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-deepmerge/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-deepmerge/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Nick Fisher"
    },
    "bugs": {
        "url": "https://github.com/KyleAMathews/deepmerge/issues"
    },
    "dependencies": {},
    "description": "A library for deep (recursive) merging of Javascript objects",
    "devDependencies": {
        "jsmd": "0.3.1",
        "tap": "~7.1.2"
    },
    "directories": {},
    "dist": {
        "shasum": "1663691629d4dbfe364fa12a2a4f0aa86aa3a050",
        "tarball": "https://registry.npmjs.org/deepmerge/-/deepmerge-1.3.2.tgz"
    },
    "engines": {
        "node": ">=0.10.0"
    },
    "gitHead": "bac0e9ffe72e3fda82608527a463bda5e2eae4b5",
    "homepage": "https://github.com/KyleAMathews/deepmerge",
    "keywords": [
        "merge",
        "deep",
        "extend",
        "copy",
        "clone",
        "recursive"
    ],
    "license": "MIT",
    "main": "index",
    "maintainers": [
        {
            "name": "kylemathews",
            "email": "mathews.kyle@gmail.com"
        },
        {
            "name": "macdja38",
            "email": "jakeincanada@icloud.com"
        },
        {
            "name": "nfisher",
            "email": "nfisher@trafficland.com"
        },
        {
            "name": "tehshrike",
            "email": "me@JoshDuff.com"
        }
    ],
    "name": "deepmerge",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/KyleAMathews/deepmerge.git"
    },
    "scripts": {
        "test": "tap test/*.js && jsmd README.markdown"
    },
    "version": "1.3.2"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module deepmerge](#apidoc.module.deepmerge)
1.  [function <span class="apidocSignatureSpan">deepmerge.</span>all (array, optionsArgument)](#apidoc.element.deepmerge.all)



# <a name="apidoc.module.deepmerge"></a>[module deepmerge](#apidoc.module.deepmerge)

#### <a name="apidoc.element.deepmerge.all"></a>[function <span class="apidocSignatureSpan">deepmerge.</span>all (array, optionsArgument)](#apidoc.element.deepmerge.all)
- description and source-code
```javascript
function deepmergeAll(array, optionsArgument) {
    if (!Array.isArray(array) || array.length < 2) {
        throw new Error('first argument should be an array with at least two elements')
    }

    // we are sure there are at least 2 values, so it is safe to have no initial value
    return array.reduce(function(prev, next) {
        return deepmerge(prev, next, optionsArgument)
    })
}
```
- example usage
```shell
...
elements from both 'x' and 'y'.

If an element at the same key is present for both 'x' and 'y', the value from
'y' will appear in the result.

Merging creates a new object, so that neither 'x' or 'y' are be modified.  However, child objects on 'x' or 'y' are copied over -
if you to copy all values, you must pass 'true' to the clone option.

merge.all(arrayOfObjects, [options])
-----------

Merges two or more objects into a single result object.

'''js
var x = { foo: { bar: 3 } }
var y = { foo: { baz: 4 } }
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
