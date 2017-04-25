# npmdoc-jade

#### basic api documentation for  [jade (v1.11.0)](http://jade-lang.com)  [![npm package](https://img.shields.io/npm/v/npmdoc-jade.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-jade) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-jade.svg)](https://travis-ci.org/npmdoc/node-npmdoc-jade)

#### A clean, whitespace-sensitive template language for writing HTML

[![NPM](https://nodei.co/npm/jade.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/jade)

- [https://npmdoc.github.io/node-npmdoc-jade/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-jade/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-jade/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-jade/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-jade/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-jade/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "TJ Holowaychuk"
    },
    "bin": {
        "jade": "./bin/jade.js"
    },
    "browser": {
        "fs": false,
        "./lib/filters.js": "./lib/filters-client.js"
    },
    "bugs": {
        "url": "https://github.com/jadejs/jade/issues"
    },
    "component": {
        "scripts": {
            "jade": "runtime.js"
        }
    },
    "dependencies": {
        "character-parser": "1.2.1",
        "clean-css": "^3.1.9",
        "commander": "~2.6.0",
        "constantinople": "~3.0.1",
        "jstransformer": "0.0.2",
        "mkdirp": "~0.5.0",
        "transformers": "2.1.0",
        "uglify-js": "^2.4.19",
        "void-elements": "~2.0.1",
        "with": "~4.0.0"
    },
    "deprecated": "Jade has been renamed to pug, please install the latest version of pug instead of jade",
    "description": "A clean, whitespace-sensitive template language for writing HTML",
    "devDependencies": {
        "browserify": "*",
        "browserify-middleware": "~4.1.0",
        "code-mirror": "~3.22.0",
        "coffee-script": "*",
        "coveralls": "^2.11.2",
        "express": "~4.10.4",
        "github-basic": "^4.1.2",
        "handle": "~1.0.0",
        "highlight-codemirror": "~4.1.0",
        "inconsolata": "0.0.2",
        "istanbul": "*",
        "jade-code-mirror": "~1.0.5",
        "jade-highlighter": "~1.0.5",
        "jstransformer-cdata": "0.0.3",
        "jstransformer-coffee-script": "0.0.2",
        "jstransformer-less": "^1.0.0",
        "jstransformer-marked": "0.0.1",
        "jstransformer-stylus": "0.0.1",
        "jstransformer-verbatim": "0.0.2",
        "less": "<2.0.0",
        "less-file": "0.0.9",
        "linify": "*",
        "lsr": "^1.0.0",
        "marked": "~0.3.3",
        "mocha": "*",
        "opener": "^1.3.0",
        "pull-request": "^3.0.0",
        "rimraf": "^2.2.8",
        "should": "*",
        "stop": "^3.0.0-rc1",
        "stylus": "*",
        "twbs": "0.0.6",
        "uglify-js": "*"
    },
    "directories": {},
    "dist": {
        "shasum": "9c80e538c12d3fb95c8d9bb9559fa0cc040405fd",
        "tarball": "https://registry.npmjs.org/jade/-/jade-1.11.0.tgz"
    },
    "gitHead": "31966399f86b15159f2ff47dff99fbf4c92fadd5",
    "homepage": "http://jade-lang.com",
    "license": "MIT",
    "main": "lib",
    "maintainers": [
        {
            "name": "forbeslindesay"
        },
        {
            "name": "bloodyowl"
        },
        {
            "name": "jbnicolai"
        },
        {
            "name": "alubbe"
        }
    ],
    "name": "jade",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git://github.com/jadejs/jade.git"
    },
    "scripts": {
        "build": "npm run compile",
        "compile": "npm run compile-full && npm run compile-runtime",
        "compile-full": "browserify ./lib/index.js --standalone jade -x ./node_modules/transformers > jade.js",
        "compile-runtime": "browserify ./lib/runtime.js --standalone jade > runtime.js",
        "coverage": "istanbul cover --report none --dir cov-pt0 node_modules/mocha/bin/_mocha -- -R dot",
        "coveralls": "npm run coverage && cat ./coverage/lcov.info | coveralls",
        "postcoverage": "istanbul report --include cov-pt\\*/coverage.json && rimraf cov-pt*",
        "precoverage": "rimraf coverage && rimraf cov-pt*",
        "prepublish": "npm prune && linify transform bin && npm run build",
        "test": "mocha -R spec"
    },
    "version": "1.11.0"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
