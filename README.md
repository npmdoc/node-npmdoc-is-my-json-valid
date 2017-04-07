# api documentation for  [is-my-json-valid (v2.16.0)](https://github.com/mafintosh/is-my-json-valid)  [![npm package](https://img.shields.io/npm/v/npmdoc-is-my-json-valid.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-is-my-json-valid) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-is-my-json-valid.svg)](https://travis-ci.org/npmdoc/node-npmdoc-is-my-json-valid)
#### A JSONSchema validator that uses code generation to be extremely fast

[![NPM](https://nodei.co/npm/is-my-json-valid.png?downloads=true)](https://www.npmjs.com/package/is-my-json-valid)

[![apidoc](https://npmdoc.github.io/node-npmdoc-is-my-json-valid/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-is-my-json-valid_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-is-my-json-valid/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-is-my-json-valid/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-is-my-json-valid/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Mathias Buus"
    },
    "bugs": {
        "url": "https://github.com/mafintosh/is-my-json-valid/issues"
    },
    "dependencies": {
        "generate-function": "^2.0.0",
        "generate-object-property": "^1.1.0",
        "jsonpointer": "^4.0.0",
        "xtend": "^4.0.0"
    },
    "description": "A JSONSchema validator that uses code generation to be extremely fast",
    "devDependencies": {
        "tape": "^2.13.4"
    },
    "directories": {},
    "dist": {
        "shasum": "f079dd9bfdae65ee2038aae8acbc86ab109e3693",
        "tarball": "https://registry.npmjs.org/is-my-json-valid/-/is-my-json-valid-2.16.0.tgz"
    },
    "gitHead": "01db30a6c968bfa87f2b6e16a905e73172bc6bea",
    "homepage": "https://github.com/mafintosh/is-my-json-valid",
    "keywords": [
        "json",
        "schema",
        "orderly",
        "jsonschema"
    ],
    "license": "MIT",
    "main": "index.js",
    "maintainers": [
        {
            "name": "emilbay",
            "email": "github@tixz.dk"
        },
        {
            "name": "emilbayes",
            "email": "github@tixz.dk"
        },
        {
            "name": "freeall",
            "email": "freeall@gmail.com"
        },
        {
            "name": "linusu",
            "email": "linus@folkdatorn.se"
        },
        {
            "name": "mafintosh",
            "email": "mathiasbuus@gmail.com"
        },
        {
            "name": "watson",
            "email": "w@tson.dk"
        },
        {
            "name": "yoshuawuyts",
            "email": "i@yoshuawuyts.com"
        }
    ],
    "name": "is-my-json-valid",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/mafintosh/is-my-json-valid.git"
    },
    "scripts": {
        "test": "tape test/*.js"
    },
    "version": "2.16.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module is-my-json-valid](#apidoc.module.is-my-json-valid)
1.  [function <span class="apidocSignatureSpan">is-my-json-valid.</span>filter (schema, opts)](#apidoc.element.is-my-json-valid.filter)



# <a name="apidoc.module.is-my-json-valid"></a>[module is-my-json-valid](#apidoc.module.is-my-json-valid)

#### <a name="apidoc.element.is-my-json-valid.filter"></a>[function <span class="apidocSignatureSpan">is-my-json-valid.</span>filter (schema, opts)](#apidoc.element.is-my-json-valid.filter)
- description and source-code
```javascript
filter = function (schema, opts) {
  var validate = module.exports(schema, xtend(opts, {filter: true}))
  return function(sch) {
    validate(sch)
    return sch
  }
}
```
- example usage
```shell
...
'''

## Filtering away additional properties

is-my-json-valid supports filtering away properties not in the schema

''' js
var filter = validator.filter({
  required: true,
  type: 'object',
  properties: {
    hello: {type: 'string', required: true}
  },
  additionalProperties: false
})
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
