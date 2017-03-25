# api documentation for  [jade (v1.11.0)](http://jade-lang.com)  [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-jade.svg)](https://travis-ci.org/npmdoc/node-npmdoc-jade)
#### A clean, whitespace-sensitive template language for writing HTML

[![NPM](https://nodei.co/npm/jade.png?downloads=true)](https://www.npmjs.com/package/jade)

[![apidoc](https://npmdoc.github.io/node-npmdoc-jade/build/screen-capture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-jade_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-jade/build..beta..travis-ci.org/apidoc.html)

![package-listing](https://npmdoc.github.io/node-npmdoc-jade/build/screen-capture.npmPackageListing.svg)



# package.json

```json

{
    "author": {
        "name": "TJ Holowaychuk",
        "email": "tj@vision-media.ca"
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
            "name": "forbeslindesay",
            "email": "forbes@lindesay.co.uk"
        },
        {
            "name": "bloodyowl",
            "email": "mlbli@me.com"
        },
        {
            "name": "jbnicolai",
            "email": "jappelman@xebia.com"
        },
        {
            "name": "alubbe",
            "email": "npm@lubbe.org"
        }
    ],
    "name": "jade",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
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



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module jade](#apidoc.module.jade)
1.  [function <span class="apidocSignatureSpan">jade.</span>Compiler (node, options)](#apidoc.element.jade.Compiler)
1.  [function <span class="apidocSignatureSpan">jade.</span>Lexer (str, filename)](#apidoc.element.jade.Lexer)
1.  [function <span class="apidocSignatureSpan">jade.</span>Parser (str, filename, options)](#apidoc.element.jade.Parser)
1.  [function <span class="apidocSignatureSpan">jade.</span>__express (path, options, fn)](#apidoc.element.jade.__express)
1.  [function <span class="apidocSignatureSpan">jade.</span>compile (str, options)](#apidoc.element.jade.compile)
1.  [function <span class="apidocSignatureSpan">jade.</span>compileClient (str, options)](#apidoc.element.jade.compileClient)
1.  [function <span class="apidocSignatureSpan">jade.</span>compileClientWithDependenciesTracked (str, options)](#apidoc.element.jade.compileClientWithDependenciesTracked)
1.  [function <span class="apidocSignatureSpan">jade.</span>compileFile (path, options)](#apidoc.element.jade.compileFile)
1.  [function <span class="apidocSignatureSpan">jade.</span>compileFileClient (path, options)](#apidoc.element.jade.compileFileClient)
1.  [function <span class="apidocSignatureSpan">jade.</span>filters (name, str, options)](#apidoc.element.jade.filters)
1.  [function <span class="apidocSignatureSpan">jade.</span>nodes.Block (node)](#apidoc.element.jade.nodes.Block)
1.  [function <span class="apidocSignatureSpan">jade.</span>nodes.BlockComment (val, block, buffer)](#apidoc.element.jade.nodes.BlockComment)
1.  [function <span class="apidocSignatureSpan">jade.</span>nodes.Case (expr, block)](#apidoc.element.jade.nodes.Case)
1.  [function <span class="apidocSignatureSpan">jade.</span>nodes.Code (val, buffer, escape)](#apidoc.element.jade.nodes.Code)
1.  [function <span class="apidocSignatureSpan">jade.</span>nodes.Comment (val, buffer)](#apidoc.element.jade.nodes.Comment)
1.  [function <span class="apidocSignatureSpan">jade.</span>nodes.Doctype (val)](#apidoc.element.jade.nodes.Doctype)
1.  [function <span class="apidocSignatureSpan">jade.</span>nodes.Each (obj, val, key, block)](#apidoc.element.jade.nodes.Each)
1.  [function <span class="apidocSignatureSpan">jade.</span>nodes.Filter (name, block, attrs)](#apidoc.element.jade.nodes.Filter)
1.  [function <span class="apidocSignatureSpan">jade.</span>nodes.Literal (str)](#apidoc.element.jade.nodes.Literal)
1.  [function <span class="apidocSignatureSpan">jade.</span>nodes.Mixin (name, args, block, call)](#apidoc.element.jade.nodes.Mixin)
1.  [function <span class="apidocSignatureSpan">jade.</span>nodes.MixinBlock ()](#apidoc.element.jade.nodes.MixinBlock)
1.  [function <span class="apidocSignatureSpan">jade.</span>nodes.Node ()](#apidoc.element.jade.nodes.Node)
1.  [function <span class="apidocSignatureSpan">jade.</span>nodes.Tag (name, block)](#apidoc.element.jade.nodes.Tag)
1.  [function <span class="apidocSignatureSpan">jade.</span>nodes.Text (line)](#apidoc.element.jade.nodes.Text)
1.  [function <span class="apidocSignatureSpan">jade.</span>render (str, options, fn)](#apidoc.element.jade.render)
1.  [function <span class="apidocSignatureSpan">jade.</span>renderFile (path, options, fn)](#apidoc.element.jade.renderFile)
1.  object <span class="apidocSignatureSpan">jade.</span>Compiler.prototype
1.  object <span class="apidocSignatureSpan">jade.</span>Lexer.prototype
1.  object <span class="apidocSignatureSpan">jade.</span>Parser.prototype
1.  object <span class="apidocSignatureSpan">jade.</span>cache
1.  object <span class="apidocSignatureSpan">jade.</span>doctypes
1.  object <span class="apidocSignatureSpan">jade.</span>nodes
1.  object <span class="apidocSignatureSpan">jade.</span>nodes.Block.prototype
1.  object <span class="apidocSignatureSpan">jade.</span>nodes.BlockComment.prototype
1.  object <span class="apidocSignatureSpan">jade.</span>nodes.Case.When.prototype
1.  object <span class="apidocSignatureSpan">jade.</span>nodes.Case.prototype
1.  object <span class="apidocSignatureSpan">jade.</span>nodes.Code.prototype
1.  object <span class="apidocSignatureSpan">jade.</span>nodes.Comment.prototype
1.  object <span class="apidocSignatureSpan">jade.</span>nodes.Doctype.prototype
1.  object <span class="apidocSignatureSpan">jade.</span>nodes.Each.prototype
1.  object <span class="apidocSignatureSpan">jade.</span>nodes.Filter.prototype
1.  object <span class="apidocSignatureSpan">jade.</span>nodes.Literal.prototype
1.  object <span class="apidocSignatureSpan">jade.</span>nodes.Mixin.prototype
1.  object <span class="apidocSignatureSpan">jade.</span>nodes.MixinBlock.prototype
1.  object <span class="apidocSignatureSpan">jade.</span>nodes.Node.prototype
1.  object <span class="apidocSignatureSpan">jade.</span>nodes.Tag.prototype
1.  object <span class="apidocSignatureSpan">jade.</span>nodes.Text.prototype
1.  object <span class="apidocSignatureSpan">jade.</span>runtime
1.  object <span class="apidocSignatureSpan">jade.</span>selfClosing
1.  object <span class="apidocSignatureSpan">jade.</span>utils

#### [module jade.Compiler](#apidoc.module.jade.Compiler)
1.  [function <span class="apidocSignatureSpan">jade.</span>Compiler (node, options)](#apidoc.element.jade.Compiler.Compiler)

#### [module jade.Compiler.prototype](#apidoc.module.jade.Compiler.prototype)
1.  [function <span class="apidocSignatureSpan">jade.Compiler.prototype.</span>attrs (attrs, buffer)](#apidoc.element.jade.Compiler.prototype.attrs)
1.  [function <span class="apidocSignatureSpan">jade.Compiler.prototype.</span>buffer (str, interpolate)](#apidoc.element.jade.Compiler.prototype.buffer)
1.  [function <span class="apidocSignatureSpan">jade.Compiler.prototype.</span>bufferExpression (src)](#apidoc.element.jade.Compiler.prototype.bufferExpression)
1.  [function <span class="apidocSignatureSpan">jade.Compiler.prototype.</span>compile ()](#apidoc.element.jade.Compiler.prototype.compile)
1.  [function <span class="apidocSignatureSpan">jade.Compiler.prototype.</span>prettyIndent (offset, newline)](#apidoc.element.jade.Compiler.prototype.prettyIndent)
1.  [function <span class="apidocSignatureSpan">jade.Compiler.prototype.</span>setDoctype (name)](#apidoc.element.jade.Compiler.prototype.setDoctype)
1.  [function <span class="apidocSignatureSpan">jade.Compiler.prototype.</span>visit (node)](#apidoc.element.jade.Compiler.prototype.visit)
1.  [function <span class="apidocSignatureSpan">jade.Compiler.prototype.</span>visitAttributes (attrs, attributeBlocks)](#apidoc.element.jade.Compiler.prototype.visitAttributes)
1.  [function <span class="apidocSignatureSpan">jade.Compiler.prototype.</span>visitBlock (block)](#apidoc.element.jade.Compiler.prototype.visitBlock)
1.  [function <span class="apidocSignatureSpan">jade.Compiler.prototype.</span>visitBlockComment (comment)](#apidoc.element.jade.Compiler.prototype.visitBlockComment)
1.  [function <span class="apidocSignatureSpan">jade.Compiler.prototype.</span>visitCase (node)](#apidoc.element.jade.Compiler.prototype.visitCase)
1.  [function <span class="apidocSignatureSpan">jade.Compiler.prototype.</span>visitCode (code)](#apidoc.element.jade.Compiler.prototype.visitCode)
1.  [function <span class="apidocSignatureSpan">jade.Compiler.prototype.</span>visitComment (comment)](#apidoc.element.jade.Compiler.prototype.visitComment)
1.  [function <span class="apidocSignatureSpan">jade.Compiler.prototype.</span>visitDoctype (doctype)](#apidoc.element.jade.Compiler.prototype.visitDoctype)
1.  [function <span class="apidocSignatureSpan">jade.Compiler.prototype.</span>visitEach (each)](#apidoc.element.jade.Compiler.prototype.visitEach)
1.  [function <span class="apidocSignatureSpan">jade.Compiler.prototype.</span>visitFilter (filter)](#apidoc.element.jade.Compiler.prototype.visitFilter)
1.  [function <span class="apidocSignatureSpan">jade.Compiler.prototype.</span>visitLiteral (node)](#apidoc.element.jade.Compiler.prototype.visitLiteral)
1.  [function <span class="apidocSignatureSpan">jade.Compiler.prototype.</span>visitMixin (mixin)](#apidoc.element.jade.Compiler.prototype.visitMixin)
1.  [function <span class="apidocSignatureSpan">jade.Compiler.prototype.</span>visitMixinBlock (block)](#apidoc.element.jade.Compiler.prototype.visitMixinBlock)
1.  [function <span class="apidocSignatureSpan">jade.Compiler.prototype.</span>visitNode (node)](#apidoc.element.jade.Compiler.prototype.visitNode)
1.  [function <span class="apidocSignatureSpan">jade.Compiler.prototype.</span>visitTag (tag)](#apidoc.element.jade.Compiler.prototype.visitTag)
1.  [function <span class="apidocSignatureSpan">jade.Compiler.prototype.</span>visitText (text)](#apidoc.element.jade.Compiler.prototype.visitText)
1.  [function <span class="apidocSignatureSpan">jade.Compiler.prototype.</span>visitWhen (node)](#apidoc.element.jade.Compiler.prototype.visitWhen)

#### [module jade.Lexer](#apidoc.module.jade.Lexer)
1.  [function <span class="apidocSignatureSpan">jade.</span>Lexer (str, filename)](#apidoc.element.jade.Lexer.Lexer)

#### [module jade.Lexer.prototype](#apidoc.module.jade.Lexer.prototype)
1.  [function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>advance ()](#apidoc.element.jade.Lexer.prototype.advance)
1.  [function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>append ()](#apidoc.element.jade.Lexer.prototype.append)
1.  [function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>attributesBlock ()](#apidoc.element.jade.Lexer.prototype.attributesBlock)
1.  [function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>attrs ()](#apidoc.element.jade.Lexer.prototype.attrs)
1.  [function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>blank ()](#apidoc.element.jade.Lexer.prototype.blank)
1.  [function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>block ()](#apidoc.element.jade.Lexer.prototype.block)
1.  [function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>blockCode ()](#apidoc.element.jade.Lexer.prototype.blockCode)
1.  [function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>bracketExpression (skip)](#apidoc.element.jade.Lexer.prototype.bracketExpression)
1.  [function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>call ()](#apidoc.element.jade.Lexer.prototype.call)
1.  [function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>case ()](#apidoc.element.jade.Lexer.prototype.case)
1.  [function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>className ()](#apidoc.element.jade.Lexer.prototype.className)
1.  [function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>code ()](#apidoc.element.jade.Lexer.prototype.code)
1.  [function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>colon ()](#apidoc.element.jade.Lexer.prototype.colon)
1.  [function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>comment ()](#apidoc.element.jade.Lexer.prototype.comment)
1.  [function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>conditional ()](#apidoc.element.jade.Lexer.prototype.conditional)
1.  [function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>consume (len)](#apidoc.element.jade.Lexer.prototype.consume)
1.  [function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>default ()](#apidoc.element.jade.Lexer.prototype.default)
1.  [function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>defer (tok)](#apidoc.element.jade.Lexer.prototype.defer)
1.  [function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>deferred ()](#apidoc.element.jade.Lexer.prototype.deferred)
1.  [function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>doctype ()](#apidoc.element.jade.Lexer.prototype.doctype)
1.  [function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>dot ()](#apidoc.element.jade.Lexer.prototype.dot)
1.  [function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>each ()](#apidoc.element.jade.Lexer.prototype.each)
1.  [function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>eos ()](#apidoc.element.jade.Lexer.prototype.eos)
1.  [function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>extends ()](#apidoc.element.jade.Lexer.prototype.extends)
1.  [function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>fail ()](#apidoc.element.jade.Lexer.prototype.fail)
1.  [function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>filter ()](#apidoc.element.jade.Lexer.prototype.filter)
1.  [function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>id ()](#apidoc.element.jade.Lexer.prototype.id)
1.  [function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>include ()](#apidoc.element.jade.Lexer.prototype.include)
1.  [function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>includeFiltered ()](#apidoc.element.jade.Lexer.prototype.includeFiltered)
1.  [function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>indent ()](#apidoc.element.jade.Lexer.prototype.indent)
1.  [function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>interpolation ()](#apidoc.element.jade.Lexer.prototype.interpolation)
1.  [function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>lookahead (n)](#apidoc.element.jade.Lexer.prototype.lookahead)
1.  [function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>mixin ()](#apidoc.element.jade.Lexer.prototype.mixin)
1.  [function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>mixinBlock ()](#apidoc.element.jade.Lexer.prototype.mixinBlock)
1.  [function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>next ()](#apidoc.element.jade.Lexer.prototype.next)
1.  [function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>pipelessText ()](#apidoc.element.jade.Lexer.prototype.pipelessText)
1.  [function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>prepend ()](#apidoc.element.jade.Lexer.prototype.prepend)
1.  [function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>scan (regexp, type)](#apidoc.element.jade.Lexer.prototype.scan)
1.  [function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>stashed ()](#apidoc.element.jade.Lexer.prototype.stashed)
1.  [function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>tag ()](#apidoc.element.jade.Lexer.prototype.tag)
1.  [function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>text ()](#apidoc.element.jade.Lexer.prototype.text)
1.  [function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>textFail ()](#apidoc.element.jade.Lexer.prototype.textFail)
1.  [function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>tok (type, val)](#apidoc.element.jade.Lexer.prototype.tok)
1.  [function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>when ()](#apidoc.element.jade.Lexer.prototype.when)
1.  [function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>while ()](#apidoc.element.jade.Lexer.prototype.while)
1.  [function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>yield ()](#apidoc.element.jade.Lexer.prototype.yield)

#### [module jade.Parser](#apidoc.module.jade.Parser)
1.  [function <span class="apidocSignatureSpan">jade.</span>Parser (str, filename, options)](#apidoc.element.jade.Parser.Parser)

#### [module jade.Parser.prototype](#apidoc.module.jade.Parser.prototype)
1.  [function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>accept (type)](#apidoc.element.jade.Parser.prototype.accept)
1.  [function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>advance ()](#apidoc.element.jade.Parser.prototype.advance)
1.  [function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>block ()](#apidoc.element.jade.Parser.prototype.block)
1.  [function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>constructor (str, filename, options)](#apidoc.element.jade.Parser.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>context (parser)](#apidoc.element.jade.Parser.prototype.context)
1.  [function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>expect (type)](#apidoc.element.jade.Parser.prototype.expect)
1.  [function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>line ()](#apidoc.element.jade.Parser.prototype.line)
1.  [function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>lookahead (n)](#apidoc.element.jade.Parser.prototype.lookahead)
1.  [function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>parse ()](#apidoc.element.jade.Parser.prototype.parse)
1.  [function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>parseBlock ()](#apidoc.element.jade.Parser.prototype.parseBlock)
1.  [function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>parseBlockCode ()](#apidoc.element.jade.Parser.prototype.parseBlockCode)
1.  [function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>parseBlockExpansion ()](#apidoc.element.jade.Parser.prototype.parseBlockExpansion)
1.  [function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>parseCall ()](#apidoc.element.jade.Parser.prototype.parseCall)
1.  [function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>parseCase ()](#apidoc.element.jade.Parser.prototype.parseCase)
1.  [function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>parseCode (afterIf)](#apidoc.element.jade.Parser.prototype.parseCode)
1.  [function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>parseComment ()](#apidoc.element.jade.Parser.prototype.parseComment)
1.  [function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>parseDefault ()](#apidoc.element.jade.Parser.prototype.parseDefault)
1.  [function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>parseDoctype ()](#apidoc.element.jade.Parser.prototype.parseDoctype)
1.  [function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>parseEach ()](#apidoc.element.jade.Parser.prototype.parseEach)
1.  [function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>parseExpr ()](#apidoc.element.jade.Parser.prototype.parseExpr)
1.  [function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>parseExtends ()](#apidoc.element.jade.Parser.prototype.parseExtends)
1.  [function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>parseFilter ()](#apidoc.element.jade.Parser.prototype.parseFilter)
1.  [function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>parseInclude ()](#apidoc.element.jade.Parser.prototype.parseInclude)
1.  [function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>parseInlineTagsInText (str)](#apidoc.element.jade.Parser.prototype.parseInlineTagsInText)
1.  [function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>parseInterpolation ()](#apidoc.element.jade.Parser.prototype.parseInterpolation)
1.  [function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>parseMixin ()](#apidoc.element.jade.Parser.prototype.parseMixin)
1.  [function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>parseMixinBlock ()](#apidoc.element.jade.Parser.prototype.parseMixinBlock)
1.  [function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>parseTag ()](#apidoc.element.jade.Parser.prototype.parseTag)
1.  [function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>parseText ()](#apidoc.element.jade.Parser.prototype.parseText)
1.  [function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>parseTextBlock ()](#apidoc.element.jade.Parser.prototype.parseTextBlock)
1.  [function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>parseWhen ()](#apidoc.element.jade.Parser.prototype.parseWhen)
1.  [function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>peek ()](#apidoc.element.jade.Parser.prototype.peek)
1.  [function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>resolvePath (path, purpose)](#apidoc.element.jade.Parser.prototype.resolvePath)
1.  [function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>tag (tag)](#apidoc.element.jade.Parser.prototype.tag)

#### [module jade.nodes](#apidoc.module.jade.nodes)
1.  [function <span class="apidocSignatureSpan">jade.nodes.</span>Block (node)](#apidoc.element.jade.nodes.Block)
1.  [function <span class="apidocSignatureSpan">jade.nodes.</span>BlockComment (val, block, buffer)](#apidoc.element.jade.nodes.BlockComment)
1.  [function <span class="apidocSignatureSpan">jade.nodes.</span>Case (expr, block)](#apidoc.element.jade.nodes.Case)
1.  [function <span class="apidocSignatureSpan">jade.nodes.</span>Code (val, buffer, escape)](#apidoc.element.jade.nodes.Code)
1.  [function <span class="apidocSignatureSpan">jade.nodes.</span>Comment (val, buffer)](#apidoc.element.jade.nodes.Comment)
1.  [function <span class="apidocSignatureSpan">jade.nodes.</span>Doctype (val)](#apidoc.element.jade.nodes.Doctype)
1.  [function <span class="apidocSignatureSpan">jade.nodes.</span>Each (obj, val, key, block)](#apidoc.element.jade.nodes.Each)
1.  [function <span class="apidocSignatureSpan">jade.nodes.</span>Filter (name, block, attrs)](#apidoc.element.jade.nodes.Filter)
1.  [function <span class="apidocSignatureSpan">jade.nodes.</span>Literal (str)](#apidoc.element.jade.nodes.Literal)
1.  [function <span class="apidocSignatureSpan">jade.nodes.</span>Mixin (name, args, block, call)](#apidoc.element.jade.nodes.Mixin)
1.  [function <span class="apidocSignatureSpan">jade.nodes.</span>MixinBlock ()](#apidoc.element.jade.nodes.MixinBlock)
1.  [function <span class="apidocSignatureSpan">jade.nodes.</span>Node ()](#apidoc.element.jade.nodes.Node)
1.  [function <span class="apidocSignatureSpan">jade.nodes.</span>Tag (name, block)](#apidoc.element.jade.nodes.Tag)
1.  [function <span class="apidocSignatureSpan">jade.nodes.</span>Text (line)](#apidoc.element.jade.nodes.Text)

#### [module jade.nodes.Block](#apidoc.module.jade.nodes.Block)
1.  [function <span class="apidocSignatureSpan">jade.nodes.</span>Block (node)](#apidoc.element.jade.nodes.Block.Block)

#### [module jade.nodes.Block.prototype](#apidoc.module.jade.nodes.Block.prototype)
1.  boolean <span class="apidocSignatureSpan">jade.nodes.Block.prototype.</span>isBlock
1.  [function <span class="apidocSignatureSpan">jade.nodes.Block.prototype.</span>clone ()](#apidoc.element.jade.nodes.Block.prototype.clone)
1.  [function <span class="apidocSignatureSpan">jade.nodes.Block.prototype.</span>constructor (node)](#apidoc.element.jade.nodes.Block.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">jade.nodes.Block.prototype.</span>includeBlock ()](#apidoc.element.jade.nodes.Block.prototype.includeBlock)
1.  [function <span class="apidocSignatureSpan">jade.nodes.Block.prototype.</span>isEmpty ()](#apidoc.element.jade.nodes.Block.prototype.isEmpty)
1.  [function <span class="apidocSignatureSpan">jade.nodes.Block.prototype.</span>push (node)](#apidoc.element.jade.nodes.Block.prototype.push)
1.  [function <span class="apidocSignatureSpan">jade.nodes.Block.prototype.</span>replace (other)](#apidoc.element.jade.nodes.Block.prototype.replace)
1.  [function <span class="apidocSignatureSpan">jade.nodes.Block.prototype.</span>unshift (node)](#apidoc.element.jade.nodes.Block.prototype.unshift)
1.  string <span class="apidocSignatureSpan">jade.nodes.Block.prototype.</span>type

#### [module jade.nodes.BlockComment](#apidoc.module.jade.nodes.BlockComment)
1.  [function <span class="apidocSignatureSpan">jade.nodes.</span>BlockComment (val, block, buffer)](#apidoc.element.jade.nodes.BlockComment.BlockComment)

#### [module jade.nodes.BlockComment.prototype](#apidoc.module.jade.nodes.BlockComment.prototype)
1.  [function <span class="apidocSignatureSpan">jade.nodes.BlockComment.prototype.</span>constructor (val, block, buffer)](#apidoc.element.jade.nodes.BlockComment.prototype.constructor)
1.  string <span class="apidocSignatureSpan">jade.nodes.BlockComment.prototype.</span>type

#### [module jade.nodes.Case](#apidoc.module.jade.nodes.Case)
1.  [function <span class="apidocSignatureSpan">jade.nodes.</span>Case (expr, block)](#apidoc.element.jade.nodes.Case.Case)
1.  [function <span class="apidocSignatureSpan">jade.nodes.Case.</span>When (expr, block)](#apidoc.element.jade.nodes.Case.When)

#### [module jade.nodes.Case.When.prototype](#apidoc.module.jade.nodes.Case.When.prototype)
1.  [function <span class="apidocSignatureSpan">jade.nodes.Case.When.prototype.</span>constructor (expr, block)](#apidoc.element.jade.nodes.Case.When.prototype.constructor)
1.  string <span class="apidocSignatureSpan">jade.nodes.Case.When.prototype.</span>type

#### [module jade.nodes.Case.prototype](#apidoc.module.jade.nodes.Case.prototype)
1.  [function <span class="apidocSignatureSpan">jade.nodes.Case.prototype.</span>constructor (expr, block)](#apidoc.element.jade.nodes.Case.prototype.constructor)
1.  string <span class="apidocSignatureSpan">jade.nodes.Case.prototype.</span>type

#### [module jade.nodes.Code](#apidoc.module.jade.nodes.Code)
1.  [function <span class="apidocSignatureSpan">jade.nodes.</span>Code (val, buffer, escape)](#apidoc.element.jade.nodes.Code.Code)

#### [module jade.nodes.Code.prototype](#apidoc.module.jade.nodes.Code.prototype)
1.  [function <span class="apidocSignatureSpan">jade.nodes.Code.prototype.</span>constructor (val, buffer, escape)](#apidoc.element.jade.nodes.Code.prototype.constructor)
1.  string <span class="apidocSignatureSpan">jade.nodes.Code.prototype.</span>type

#### [module jade.nodes.Comment](#apidoc.module.jade.nodes.Comment)
1.  [function <span class="apidocSignatureSpan">jade.nodes.</span>Comment (val, buffer)](#apidoc.element.jade.nodes.Comment.Comment)

#### [module jade.nodes.Comment.prototype](#apidoc.module.jade.nodes.Comment.prototype)
1.  [function <span class="apidocSignatureSpan">jade.nodes.Comment.prototype.</span>constructor (val, buffer)](#apidoc.element.jade.nodes.Comment.prototype.constructor)
1.  string <span class="apidocSignatureSpan">jade.nodes.Comment.prototype.</span>type

#### [module jade.nodes.Doctype](#apidoc.module.jade.nodes.Doctype)
1.  [function <span class="apidocSignatureSpan">jade.nodes.</span>Doctype (val)](#apidoc.element.jade.nodes.Doctype.Doctype)

#### [module jade.nodes.Doctype.prototype](#apidoc.module.jade.nodes.Doctype.prototype)
1.  [function <span class="apidocSignatureSpan">jade.nodes.Doctype.prototype.</span>constructor (val)](#apidoc.element.jade.nodes.Doctype.prototype.constructor)
1.  string <span class="apidocSignatureSpan">jade.nodes.Doctype.prototype.</span>type

#### [module jade.nodes.Each](#apidoc.module.jade.nodes.Each)
1.  [function <span class="apidocSignatureSpan">jade.nodes.</span>Each (obj, val, key, block)](#apidoc.element.jade.nodes.Each.Each)

#### [module jade.nodes.Each.prototype](#apidoc.module.jade.nodes.Each.prototype)
1.  [function <span class="apidocSignatureSpan">jade.nodes.Each.prototype.</span>constructor (obj, val, key, block)](#apidoc.element.jade.nodes.Each.prototype.constructor)
1.  string <span class="apidocSignatureSpan">jade.nodes.Each.prototype.</span>type

#### [module jade.nodes.Filter](#apidoc.module.jade.nodes.Filter)
1.  [function <span class="apidocSignatureSpan">jade.nodes.</span>Filter (name, block, attrs)](#apidoc.element.jade.nodes.Filter.Filter)

#### [module jade.nodes.Filter.prototype](#apidoc.module.jade.nodes.Filter.prototype)
1.  [function <span class="apidocSignatureSpan">jade.nodes.Filter.prototype.</span>constructor (name, block, attrs)](#apidoc.element.jade.nodes.Filter.prototype.constructor)
1.  string <span class="apidocSignatureSpan">jade.nodes.Filter.prototype.</span>type

#### [module jade.nodes.Literal](#apidoc.module.jade.nodes.Literal)
1.  [function <span class="apidocSignatureSpan">jade.nodes.</span>Literal (str)](#apidoc.element.jade.nodes.Literal.Literal)

#### [module jade.nodes.Literal.prototype](#apidoc.module.jade.nodes.Literal.prototype)
1.  [function <span class="apidocSignatureSpan">jade.nodes.Literal.prototype.</span>constructor (str)](#apidoc.element.jade.nodes.Literal.prototype.constructor)
1.  string <span class="apidocSignatureSpan">jade.nodes.Literal.prototype.</span>type

#### [module jade.nodes.Mixin](#apidoc.module.jade.nodes.Mixin)
1.  [function <span class="apidocSignatureSpan">jade.nodes.</span>Mixin (name, args, block, call)](#apidoc.element.jade.nodes.Mixin.Mixin)

#### [module jade.nodes.Mixin.prototype](#apidoc.module.jade.nodes.Mixin.prototype)
1.  [function <span class="apidocSignatureSpan">jade.nodes.Mixin.prototype.</span>constructor (name, args, block, call)](#apidoc.element.jade.nodes.Mixin.prototype.constructor)
1.  string <span class="apidocSignatureSpan">jade.nodes.Mixin.prototype.</span>type

#### [module jade.nodes.MixinBlock](#apidoc.module.jade.nodes.MixinBlock)
1.  [function <span class="apidocSignatureSpan">jade.nodes.</span>MixinBlock ()](#apidoc.element.jade.nodes.MixinBlock.MixinBlock)

#### [module jade.nodes.MixinBlock.prototype](#apidoc.module.jade.nodes.MixinBlock.prototype)
1.  [function <span class="apidocSignatureSpan">jade.nodes.MixinBlock.prototype.</span>constructor ()](#apidoc.element.jade.nodes.MixinBlock.prototype.constructor)
1.  string <span class="apidocSignatureSpan">jade.nodes.MixinBlock.prototype.</span>type

#### [module jade.nodes.Node](#apidoc.module.jade.nodes.Node)
1.  [function <span class="apidocSignatureSpan">jade.nodes.</span>Node ()](#apidoc.element.jade.nodes.Node.Node)

#### [module jade.nodes.Node.prototype](#apidoc.module.jade.nodes.Node.prototype)
1.  [function <span class="apidocSignatureSpan">jade.nodes.Node.prototype.</span>clone ()](#apidoc.element.jade.nodes.Node.prototype.clone)
1.  string <span class="apidocSignatureSpan">jade.nodes.Node.prototype.</span>type

#### [module jade.nodes.Tag](#apidoc.module.jade.nodes.Tag)
1.  [function <span class="apidocSignatureSpan">jade.nodes.</span>Tag (name, block)](#apidoc.element.jade.nodes.Tag.Tag)

#### [module jade.nodes.Tag.prototype](#apidoc.module.jade.nodes.Tag.prototype)
1.  [function <span class="apidocSignatureSpan">jade.nodes.Tag.prototype.</span>canInline ()](#apidoc.element.jade.nodes.Tag.prototype.canInline)
1.  [function <span class="apidocSignatureSpan">jade.nodes.Tag.prototype.</span>clone ()](#apidoc.element.jade.nodes.Tag.prototype.clone)
1.  [function <span class="apidocSignatureSpan">jade.nodes.Tag.prototype.</span>constructor (name, block)](#apidoc.element.jade.nodes.Tag.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">jade.nodes.Tag.prototype.</span>isInline ()](#apidoc.element.jade.nodes.Tag.prototype.isInline)
1.  string <span class="apidocSignatureSpan">jade.nodes.Tag.prototype.</span>type

#### [module jade.nodes.Text](#apidoc.module.jade.nodes.Text)
1.  [function <span class="apidocSignatureSpan">jade.nodes.</span>Text (line)](#apidoc.element.jade.nodes.Text.Text)

#### [module jade.nodes.Text.prototype](#apidoc.module.jade.nodes.Text.prototype)
1.  boolean <span class="apidocSignatureSpan">jade.nodes.Text.prototype.</span>isText
1.  [function <span class="apidocSignatureSpan">jade.nodes.Text.prototype.</span>constructor (line)](#apidoc.element.jade.nodes.Text.prototype.constructor)
1.  string <span class="apidocSignatureSpan">jade.nodes.Text.prototype.</span>type

#### [module jade.runtime](#apidoc.module.jade.runtime)
1.  [function <span class="apidocSignatureSpan">jade.runtime.</span>DebugItem (lineno, filename)](#apidoc.element.jade.runtime.DebugItem)
1.  [function <span class="apidocSignatureSpan">jade.runtime.</span>attr (key, val, escaped, terse)](#apidoc.element.jade.runtime.attr)
1.  [function <span class="apidocSignatureSpan">jade.runtime.</span>attrs (obj, terse)](#apidoc.element.jade.runtime.attrs)
1.  [function <span class="apidocSignatureSpan">jade.runtime.</span>cls (classes, escaped)](#apidoc.element.jade.runtime.cls)
1.  [function <span class="apidocSignatureSpan">jade.runtime.</span>escape (html)](#apidoc.element.jade.runtime.escape)
1.  [function <span class="apidocSignatureSpan">jade.runtime.</span>joinClasses (val)](#apidoc.element.jade.runtime.joinClasses)
1.  [function <span class="apidocSignatureSpan">jade.runtime.</span>merge (a, b)](#apidoc.element.jade.runtime.merge)
1.  [function <span class="apidocSignatureSpan">jade.runtime.</span>rethrow (err, filename, lineno, str)](#apidoc.element.jade.runtime.rethrow)
1.  [function <span class="apidocSignatureSpan">jade.runtime.</span>style (val)](#apidoc.element.jade.runtime.style)

#### [module jade.utils](#apidoc.module.jade.utils)
1.  [function <span class="apidocSignatureSpan">jade.utils.</span>merge (a, b)](#apidoc.element.jade.utils.merge)
1.  [function <span class="apidocSignatureSpan">jade.utils.</span>stringify (str)](#apidoc.element.jade.utils.stringify)
1.  [function <span class="apidocSignatureSpan">jade.utils.</span>walkAST (ast, before, after)](#apidoc.element.jade.utils.walkAST)



# <a name="apidoc.module.jade"></a>[module jade](#apidoc.module.jade)

#### <a name="apidoc.element.jade.Compiler"></a>[function <span class="apidocSignatureSpan">jade.</span>Compiler (node, options)](#apidoc.element.jade.Compiler)
- description and source-code
```javascript
function Compiler(node, options) {
  this.options = options = options || {};
  this.node = node;
  this.hasCompiledDoctype = false;
  this.hasCompiledTag = false;
  this.pp = options.pretty || false;
  if (this.pp && typeof this.pp !== 'string') {
    this.pp = '  ';
  }
  this.debug = false !== options.compileDebug;
  this.indents = 0;
  this.parentIndents = 0;
  this.terse = false;
  this.mixins = {};
  this.dynamicMixins = false;
  if (options.doctype) this.setDoctype(options.doctype);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Lexer"></a>[function <span class="apidocSignatureSpan">jade.</span>Lexer (str, filename)](#apidoc.element.jade.Lexer)
- description and source-code
```javascript
function Lexer(str, filename) {
  this.input = str.replace(/\r\n|\r/g, '\n');
  this.filename = filename;
  this.deferredTokens = [];
  this.lastIndents = 0;
  this.lineno = 1;
  this.stash = [];
  this.indentStack = [];
  this.indentRe = null;
  this.pipeless = false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Parser"></a>[function <span class="apidocSignatureSpan">jade.</span>Parser (str, filename, options)](#apidoc.element.jade.Parser)
- description and source-code
```javascript
function Parser(str, filename, options){
  //Strip any UTF-8 BOM off of the start of 'str', if it exists.
  this.input = str.replace(/^\uFEFF/, '');
  this.lexer = new Lexer(this.input, filename);
  this.filename = filename;
  this.blocks = {};
  this.mixins = {};
  this.options = options;
  this.contexts = [this];
  this.inMixin = 0;
  this.dependencies = [];
  this.inBlock = 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.__express"></a>[function <span class="apidocSignatureSpan">jade.</span>__express (path, options, fn)](#apidoc.element.jade.__express)
- description and source-code
```javascript
__express = function (path, options, fn) {
  if(options.compileDebug == undefined && process.env.NODE_ENV === 'production') {
    options.compileDebug = false;
  }
  exports.renderFile(path, options, fn);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.compile"></a>[function <span class="apidocSignatureSpan">jade.</span>compile (str, options)](#apidoc.element.jade.compile)
- description and source-code
```javascript
compile = function (str, options){
  var options = options || {}
    , filename = options.filename
      ? utils.stringify(options.filename)
      : 'undefined'
    , fn;

  str = String(str);

  var parsed = parse(str, options);
  if (options.compileDebug !== false) {
    fn = [
        'var jade_debug = [ new jade.DebugItem( 1, ' + filename + ' ) ];'
      , 'try {'
      , parsed.body
      , '} catch (err) {'
      , '  jade.rethrow(err, jade_debug[0].filename, jade_debug[0].lineno' + (options.compileDebug === true ? ',' + utils.stringify
(str) : '') + ');'
      , '}'
    ].join('\n');
  } else {
    fn = parsed.body;
  }
  fn = new Function('locals, jade', fn)
  var res = function(locals){ return fn(locals, Object.create(runtime)) };
  if (options.client) {
    res.toString = function () {
      var err = new Error('The 'client' option is deprecated, use the 'jade.compileClient' method instead');
      err.name = 'Warning';
      console.error(err.stack || /* istanbul ignore next */ err.message);
      return exports.compileClient(str, options);
    };
  }
  res.dependencies = parsed.dependencies;
  return res;
}
```
- example usage
```shell
...

For full API, see [jade-lang.com/api](http://jade-lang.com/api/)

'''js
var jade = require('jade');

// compile
var fn = jade.compile('string of jade', options);
var html = fn(locals);

// render
var html = jade.render('string of jade', merge(options, locals));

// renderFile
var html = jade.renderFile('filename.jade', merge(options, locals));
...
```

#### <a name="apidoc.element.jade.compileClient"></a>[function <span class="apidocSignatureSpan">jade.</span>compileClient (str, options)](#apidoc.element.jade.compileClient)
- description and source-code
```javascript
compileClient = function (str, options) {
  return exports.compileClientWithDependenciesTracked(str, options).body;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.compileClientWithDependenciesTracked"></a>[function <span class="apidocSignatureSpan">jade.</span>compileClientWithDependenciesTracked (str, options)](#apidoc.element.jade.compileClientWithDependenciesTracked)
- description and source-code
```javascript
compileClientWithDependenciesTracked = function (str, options){
  var options = options || {};
  var name = options.name || 'template';
  var filename = options.filename ? utils.stringify(options.filename) : 'undefined';
  var fn;

  str = String(str);
  options.compileDebug = options.compileDebug ? true : false;
  var parsed = parse(str, options);
  if (options.compileDebug) {
    fn = [
        'var jade_debug = [ new jade.DebugItem( 1, ' + filename + ' ) ];'
      , 'try {'
      , parsed.body
      , '} catch (err) {'
      , '  jade.rethrow(err, jade_debug[0].filename, jade_debug[0].lineno, ' + utils.stringify(str) + ');'
      , '}'
    ].join('\n');
  } else {
    fn = parsed.body;
  }

  return {body: 'function ' + name + '(locals) {\n' + fn + '\n}', dependencies: parsed.dependencies};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.compileFile"></a>[function <span class="apidocSignatureSpan">jade.</span>compileFile (path, options)](#apidoc.element.jade.compileFile)
- description and source-code
```javascript
compileFile = function (path, options) {
  options = options || {};
  options.filename = path;
  return handleTemplateCache(options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.compileFileClient"></a>[function <span class="apidocSignatureSpan">jade.</span>compileFileClient (path, options)](#apidoc.element.jade.compileFileClient)
- description and source-code
```javascript
compileFileClient = function (path, options){
  var key = path + ':client';
  options = options || {};

  options.filename = path;

  if (options.cache && exports.cache[key]) {
    return exports.cache[key];
  }

  var str = fs.readFileSync(options.filename, 'utf8');
  var out = exports.compileClient(str, options);
  if (options.cache) exports.cache[key] = out;
  return out;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.filters"></a>[function <span class="apidocSignatureSpan">jade.</span>filters (name, str, options)](#apidoc.element.jade.filters)
- description and source-code
```javascript
function filter(name, str, options) {
  if (typeof filter[name] === 'function') {
    return filter[name](str, options);
  } else {
    var tr;
    try {
      tr = jstransformer(require('jstransformer-' + name));
    } catch (ex) {}
    if (tr) {
      // TODO: we may want to add a way for people to separately specify "locals"
      var result = tr.render(str, options, options).body;
      if (options && options.minify) {
        try {
          switch (tr.outputFormat) {
            case 'js':
              result = uglify.minify(result, {fromString: true}).code;
              break;
            case 'css':
              result = new CleanCSS().minify(result).styles;
              break;
          }
        } catch (ex) {
          // better to fail to minify than output nothing
        }
      }
      return result;
    } else if (transformers[name]) {
      if (!warned[name]) {
        warned[name] = true;
        if (name === 'md' || name === 'markdown') {
          var implementation = getMarkdownImplementation();
          console.log('Transformers.' + name + ' is deprecated, you must replace the :' +
                      name + ' jade filter, with :' +
                      implementation + ' and install jstransformer-' +
                      implementation + ' before you update to jade@2.0.0.');
        } else if (alternatives[name]) {
          console.log('Transformers.' + name + ' is deprecated, you must replace the :' +
                      name + ' jade filter, with :' +
                      alternatives[name] + ' and install jstransformer-' +
                      alternatives[name] + ' before you update to jade@2.0.0.');
        } else {
          console.log('Transformers.' + name + ' is deprecated, to continue using the :' +
                      name + ' jade filter after jade@2.0.0, you will need to install jstransformer-' +
                      name.toLowerCase() + '.');
        }
      }
      return transformers[name].renderSync(str, options);
    } else {
      throw new Error('unknown filter ":' + name + '"');
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.nodes.Block"></a>[function <span class="apidocSignatureSpan">jade.</span>nodes.Block (node)](#apidoc.element.jade.nodes.Block)
- description and source-code
```javascript
function Block(node){
  this.nodes = [];
  if (node) this.push(node);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.nodes.BlockComment"></a>[function <span class="apidocSignatureSpan">jade.</span>nodes.BlockComment (val, block, buffer)](#apidoc.element.jade.nodes.BlockComment)
- description and source-code
```javascript
function BlockComment(val, block, buffer) {
  this.block = block;
  this.val = val;
  this.buffer = buffer;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.nodes.Case"></a>[function <span class="apidocSignatureSpan">jade.</span>nodes.Case (expr, block)](#apidoc.element.jade.nodes.Case)
- description and source-code
```javascript
function Case(expr, block){
  this.expr = expr;
  this.block = block;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.nodes.Code"></a>[function <span class="apidocSignatureSpan">jade.</span>nodes.Code (val, buffer, escape)](#apidoc.element.jade.nodes.Code)
- description and source-code
```javascript
function Code(val, buffer, escape) {
  this.val = val;
  this.buffer = buffer;
  this.escape = escape;
  if (val.match(/^ *else/)) this.debug = false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.nodes.Comment"></a>[function <span class="apidocSignatureSpan">jade.</span>nodes.Comment (val, buffer)](#apidoc.element.jade.nodes.Comment)
- description and source-code
```javascript
function Comment(val, buffer) {
  this.val = val;
  this.buffer = buffer;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.nodes.Doctype"></a>[function <span class="apidocSignatureSpan">jade.</span>nodes.Doctype (val)](#apidoc.element.jade.nodes.Doctype)
- description and source-code
```javascript
function Doctype(val) {
  this.val = val;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.nodes.Each"></a>[function <span class="apidocSignatureSpan">jade.</span>nodes.Each (obj, val, key, block)](#apidoc.element.jade.nodes.Each)
- description and source-code
```javascript
function Each(obj, val, key, block) {
  this.obj = obj;
  this.val = val;
  this.key = key;
  this.block = block;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.nodes.Filter"></a>[function <span class="apidocSignatureSpan">jade.</span>nodes.Filter (name, block, attrs)](#apidoc.element.jade.nodes.Filter)
- description and source-code
```javascript
function Filter(name, block, attrs) {
  this.name = name;
  this.block = block;
  this.attrs = attrs;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.nodes.Literal"></a>[function <span class="apidocSignatureSpan">jade.</span>nodes.Literal (str)](#apidoc.element.jade.nodes.Literal)
- description and source-code
```javascript
function Literal(str) {
  this.str = str;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.nodes.Mixin"></a>[function <span class="apidocSignatureSpan">jade.</span>nodes.Mixin (name, args, block, call)](#apidoc.element.jade.nodes.Mixin)
- description and source-code
```javascript
function Mixin(name, args, block, call){
  Attrs.call(this);
  this.name = name;
  this.args = args;
  this.block = block;
  this.call = call;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.nodes.MixinBlock"></a>[function <span class="apidocSignatureSpan">jade.</span>nodes.MixinBlock ()](#apidoc.element.jade.nodes.MixinBlock)
- description and source-code
```javascript
function MixinBlock(){}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.nodes.Node"></a>[function <span class="apidocSignatureSpan">jade.</span>nodes.Node ()](#apidoc.element.jade.nodes.Node)
- description and source-code
```javascript
function Node(){}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.nodes.Tag"></a>[function <span class="apidocSignatureSpan">jade.</span>nodes.Tag (name, block)](#apidoc.element.jade.nodes.Tag)
- description and source-code
```javascript
function Tag(name, block) {
  Attrs.call(this);
  this.name = name;
  this.block = block || new Block;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.nodes.Text"></a>[function <span class="apidocSignatureSpan">jade.</span>nodes.Text (line)](#apidoc.element.jade.nodes.Text)
- description and source-code
```javascript
function Text(line) {
  this.val = line;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.render"></a>[function <span class="apidocSignatureSpan">jade.</span>render (str, options, fn)](#apidoc.element.jade.render)
- description and source-code
```javascript
render = function (str, options, fn){
  // support callback API
  if ('function' == typeof options) {
    fn = options, options = undefined;
  }
  if (typeof fn === 'function') {
    var res
    try {
      res = exports.render(str, options);
    } catch (ex) {
      return fn(ex);
    }
    return fn(null, res);
  }

  options = options || {};

  // cache requires .filename
  if (options.cache && !options.filename) {
    throw new Error('the "filename" option is required for caching');
  }

  return handleTemplateCache(options, str)(options);
}
```
- example usage
```shell
...
var jade = require('jade');

// compile
var fn = jade.compile('string of jade', options);
var html = fn(locals);

// render
var html = jade.render('string of jade', merge(options, locals));

// renderFile
var html = jade.renderFile('filename.jade', merge(options, locals));
'''

### Options
...
```

#### <a name="apidoc.element.jade.renderFile"></a>[function <span class="apidocSignatureSpan">jade.</span>renderFile (path, options, fn)](#apidoc.element.jade.renderFile)
- description and source-code
```javascript
renderFile = function (path, options, fn){
  // support callback API
  if ('function' == typeof options) {
    fn = options, options = undefined;
  }
  if (typeof fn === 'function') {
    var res
    try {
      res = exports.renderFile(path, options);
    } catch (ex) {
      return fn(ex);
    }
    return fn(null, res);
  }

  options = options || {};

  options.filename = path;
  return handleTemplateCache(options)(options);
}
```
- example usage
```shell
...
var fn = jade.compile('string of jade', options);
var html = fn(locals);

// render
var html = jade.render('string of jade', merge(options, locals));

// renderFile
var html = jade.renderFile('filename.jade', merge(options, locals));
'''

### Options

- 'filename'  Used in exceptions, and required when using includes
- 'compileDebug'  When 'false' no debug instrumentation is compiled
- 'pretty'    Add pretty-indentation whitespace to output _(false by default)_
...
```



# <a name="apidoc.module.jade.Compiler"></a>[module jade.Compiler](#apidoc.module.jade.Compiler)

#### <a name="apidoc.element.jade.Compiler.Compiler"></a>[function <span class="apidocSignatureSpan">jade.</span>Compiler (node, options)](#apidoc.element.jade.Compiler.Compiler)
- description and source-code
```javascript
function Compiler(node, options) {
  this.options = options = options || {};
  this.node = node;
  this.hasCompiledDoctype = false;
  this.hasCompiledTag = false;
  this.pp = options.pretty || false;
  if (this.pp && typeof this.pp !== 'string') {
    this.pp = '  ';
  }
  this.debug = false !== options.compileDebug;
  this.indents = 0;
  this.parentIndents = 0;
  this.terse = false;
  this.mixins = {};
  this.dynamicMixins = false;
  if (options.doctype) this.setDoctype(options.doctype);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jade.Compiler.prototype"></a>[module jade.Compiler.prototype](#apidoc.module.jade.Compiler.prototype)

#### <a name="apidoc.element.jade.Compiler.prototype.attrs"></a>[function <span class="apidocSignatureSpan">jade.Compiler.prototype.</span>attrs (attrs, buffer)](#apidoc.element.jade.Compiler.prototype.attrs)
- description and source-code
```javascript
attrs = function (attrs, buffer){
  var buf = [];
  var classes = [];
  var classEscaping = [];

  attrs.forEach(function(attr){
    var key = attr.name;
    var escaped = attr.escaped;

    if (key === 'class') {
      classes.push(attr.val);
      classEscaping.push(attr.escaped);
    } else if (isConstant(attr.val)) {
      if (buffer) {
        this.buffer(runtime.attr(key, toConstant(attr.val), escaped, this.terse));
      } else {
        var val = toConstant(attr.val);
        if (key === 'style') val = runtime.style(val);
        if (escaped && !(key.indexOf('data') === 0 && typeof val !== 'string')) {
          val = runtime.escape(val);
        }
        buf.push(utils.stringify(key) + ': ' + utils.stringify(val));
      }
    } else {
      if (buffer) {
        this.bufferExpression('jade.attr("' + key + '", ' + attr.val + ', ' + utils.stringify(escaped) + ', ' + utils.stringify(
this.terse) + ')');
      } else {
        var val = attr.val;
        if (key === 'style') {
          val = 'jade.style(' + val + ')';
        }
        if (escaped && !(key.indexOf('data') === 0)) {
          val = 'jade.escape(' + val + ')';
        } else if (escaped) {
          val = '(typeof (jade_interp = ' + val + ') == "string" ? jade.escape(jade_interp) : jade_interp)';
        }
        buf.push(utils.stringify(key) + ': ' + val);
      }
    }
  }.bind(this));
  if (buffer) {
    if (classes.every(isConstant)) {
      this.buffer(runtime.cls(classes.map(toConstant), classEscaping));
    } else {
      this.bufferExpression('jade.cls([' + classes.join(',') + '], ' + utils.stringify(classEscaping) + ')');
    }
  } else if (classes.length) {
    if (classes.every(isConstant)) {
      classes = utils.stringify(runtime.joinClasses(classes.map(toConstant).map(runtime.joinClasses).map(function (cls, i) {
        return classEscaping[i] ? runtime.escape(cls) : cls;
      })));
    } else {
      classes = '(jade_interp = ' + utils.stringify(classEscaping) + ',' +
        ' jade.joinClasses([' + classes.join(',') + '].map(jade.joinClasses).map(function (cls, i) {' +
        '   return jade_interp[i] ? jade.escape(cls) : cls' +
        ' }))' +
        ')';
    }
    if (classes.length)
      buf.push('"class": ' + classes);
  }
  return '{' + buf.join(',') + '}';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Compiler.prototype.buffer"></a>[function <span class="apidocSignatureSpan">jade.Compiler.prototype.</span>buffer (str, interpolate)](#apidoc.element.jade.Compiler.prototype.buffer)
- description and source-code
```javascript
buffer = function (str, interpolate) {
  var self = this;
  if (interpolate) {
    var match = /(\\)?([#!]){((?:.|\n)*)$/.exec(str);
    if (match) {
      this.buffer(str.substr(0, match.index), false);
      if (match[1]) { // escape
        this.buffer(match[2] + '{', false);
        this.buffer(match[3], true);
        return;
      } else {
        var rest = match[3];
        var range = parseJSExpression(rest);
        var code = ('!' == match[2] ? '' : 'jade.escape') + "((jade_interp = " + range.src + ") == null ? '' : jade_interp)";
        this.bufferExpression(code);
        this.buffer(rest.substr(range.end + 1), true);
        return;
      }
    }
  }

  str = utils.stringify(str);
  str = str.substr(1, str.length - 2);

  if (this.lastBufferedIdx == this.buf.length) {
    if (this.lastBufferedType === 'code') this.lastBuffered += ' + "';
    this.lastBufferedType = 'text';
    this.lastBuffered += str;
    this.buf[this.lastBufferedIdx - 1] = 'buf.push(' + this.bufferStartChar + this.lastBuffered + '");'
  } else {
    this.buf.push('buf.push("' + str + '");');
    this.lastBufferedType = 'text';
    this.bufferStartChar = '"';
    this.lastBuffered = str;
    this.lastBufferedIdx = this.buf.length;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Compiler.prototype.bufferExpression"></a>[function <span class="apidocSignatureSpan">jade.Compiler.prototype.</span>bufferExpression (src)](#apidoc.element.jade.Compiler.prototype.bufferExpression)
- description and source-code
```javascript
bufferExpression = function (src) {
  if (isConstant(src)) {
    return this.buffer(toConstant(src) + '', false)
  }
  if (this.lastBufferedIdx == this.buf.length) {
    if (this.lastBufferedType === 'text') this.lastBuffered += '"';
    this.lastBufferedType = 'code';
    this.lastBuffered += ' + (' + src + ')';
    this.buf[this.lastBufferedIdx - 1] = 'buf.push(' + this.bufferStartChar + this.lastBuffered + ');'
  } else {
    this.buf.push('buf.push(' + src + ');');
    this.lastBufferedType = 'code';
    this.bufferStartChar = '';
    this.lastBuffered = '(' + src + ')';
    this.lastBufferedIdx = this.buf.length;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Compiler.prototype.compile"></a>[function <span class="apidocSignatureSpan">jade.Compiler.prototype.</span>compile ()](#apidoc.element.jade.Compiler.prototype.compile)
- description and source-code
```javascript
compile = function (){
  this.buf = [];
  if (this.pp) this.buf.push("var jade_indent = [];");
  this.lastBufferedIdx = -1;
  this.visit(this.node);
  if (!this.dynamicMixins) {
    // if there are no dynamic mixins we can remove any un-used mixins
    var mixinNames = Object.keys(this.mixins);
    for (var i = 0; i < mixinNames.length; i++) {
      var mixin = this.mixins[mixinNames[i]];
      if (!mixin.used) {
        for (var x = 0; x < mixin.instances.length; x++) {
          for (var y = mixin.instances[x].start; y < mixin.instances[x].end; y++) {
            this.buf[y] = '';
          }
        }
      }
    }
  }
  return this.buf.join('\n');
}
```
- example usage
```shell
...

For full API, see [jade-lang.com/api](http://jade-lang.com/api/)

'''js
var jade = require('jade');

// compile
var fn = jade.compile('string of jade', options);
var html = fn(locals);

// render
var html = jade.render('string of jade', merge(options, locals));

// renderFile
var html = jade.renderFile('filename.jade', merge(options, locals));
...
```

#### <a name="apidoc.element.jade.Compiler.prototype.prettyIndent"></a>[function <span class="apidocSignatureSpan">jade.Compiler.prototype.</span>prettyIndent (offset, newline)](#apidoc.element.jade.Compiler.prototype.prettyIndent)
- description and source-code
```javascript
prettyIndent = function (offset, newline){
  offset = offset || 0;
  newline = newline ? '\n' : '';
  this.buffer(newline + Array(this.indents + offset).join(this.pp));
  if (this.parentIndents)
    this.buf.push("buf.push.apply(buf, jade_indent);");
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Compiler.prototype.setDoctype"></a>[function <span class="apidocSignatureSpan">jade.Compiler.prototype.</span>setDoctype (name)](#apidoc.element.jade.Compiler.prototype.setDoctype)
- description and source-code
```javascript
setDoctype = function (name){
  this.doctype = doctypes[name.toLowerCase()] || '<!DOCTYPE ' + name + '>';
  this.terse = this.doctype.toLowerCase() == '<!doctype html>';
  this.xml = 0 == this.doctype.indexOf('<?xml');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Compiler.prototype.visit"></a>[function <span class="apidocSignatureSpan">jade.Compiler.prototype.</span>visit (node)](#apidoc.element.jade.Compiler.prototype.visit)
- description and source-code
```javascript
visit = function (node){
  var debug = this.debug;

  if (debug) {
    this.buf.push('jade_debug.unshift(new jade.DebugItem( ' + node.line
      + ', ' + (node.filename
        ? utils.stringify(node.filename)
        : 'jade_debug[0].filename')
      + ' ));');
  }

  // Massive hack to fix our context
  // stack for - else[ if] etc
  if (false === node.debug && this.debug) {
    this.buf.pop();
    this.buf.pop();
  }

  this.visitNode(node);

  if (debug) this.buf.push('jade_debug.shift();');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Compiler.prototype.visitAttributes"></a>[function <span class="apidocSignatureSpan">jade.Compiler.prototype.</span>visitAttributes (attrs, attributeBlocks)](#apidoc.element.jade.Compiler.prototype.visitAttributes)
- description and source-code
```javascript
visitAttributes = function (attrs, attributeBlocks){
  if (attributeBlocks.length) {
    if (attrs.length) {
      var val = this.attrs(attrs);
      attributeBlocks.unshift(val);
    }
    this.bufferExpression('jade.attrs(jade.merge([' + attributeBlocks.join(',') + ']), ' + utils.stringify(this.terse) + ')');
  } else if (attrs.length) {
    this.attrs(attrs, true);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Compiler.prototype.visitBlock"></a>[function <span class="apidocSignatureSpan">jade.Compiler.prototype.</span>visitBlock (block)](#apidoc.element.jade.Compiler.prototype.visitBlock)
- description and source-code
```javascript
visitBlock = function (block){
  var len = block.nodes.length
    , escape = this.escape
    , pp = this.pp

  // Pretty print multi-line text
  if (pp && len > 1 && !escape && block.nodes[0].isText && block.nodes[1].isText)
    this.prettyIndent(1, true);

  for (var i = 0; i < len; ++i) {
    // Pretty print text
    if (pp && i > 0 && !escape && block.nodes[i].isText && block.nodes[i-1].isText)
      this.prettyIndent(1, false);

    this.visit(block.nodes[i]);
    // Multiple text nodes are separated by newlines
    if (block.nodes[i+1] && block.nodes[i].isText && block.nodes[i+1].isText)
      this.buffer('\n');
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Compiler.prototype.visitBlockComment"></a>[function <span class="apidocSignatureSpan">jade.Compiler.prototype.</span>visitBlockComment (comment)](#apidoc.element.jade.Compiler.prototype.visitBlockComment)
- description and source-code
```javascript
visitBlockComment = function (comment){
  if (!comment.buffer) return;
  if (this.pp) this.prettyIndent(1, true);
  this.buffer('<!--' + comment.val);
  this.visit(comment.block);
  if (this.pp) this.prettyIndent(1, true);
  this.buffer('-->');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Compiler.prototype.visitCase"></a>[function <span class="apidocSignatureSpan">jade.Compiler.prototype.</span>visitCase (node)](#apidoc.element.jade.Compiler.prototype.visitCase)
- description and source-code
```javascript
visitCase = function (node){
  var _ = this.withinCase;
  this.withinCase = true;
  this.buf.push('switch (' + node.expr + '){');
  this.visit(node.block);
  this.buf.push('}');
  this.withinCase = _;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Compiler.prototype.visitCode"></a>[function <span class="apidocSignatureSpan">jade.Compiler.prototype.</span>visitCode (code)](#apidoc.element.jade.Compiler.prototype.visitCode)
- description and source-code
```javascript
visitCode = function (code){
  // Wrap code blocks with {}.
  // we only wrap unbuffered code blocks ATM
  // since they are usually flow control

  // Buffer code
  if (code.buffer) {
    var val = code.val.trim();
    val = 'null == (jade_interp = '+val+') ? "" : jade_interp';
    if (code.escape) val = 'jade.escape(' + val + ')';
    this.bufferExpression(val);
  } else {
    this.buf.push(code.val);
  }

  // Block support
  if (code.block) {
    if (!code.buffer) this.buf.push('{');
    this.visit(code.block);
    if (!code.buffer) this.buf.push('}');
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Compiler.prototype.visitComment"></a>[function <span class="apidocSignatureSpan">jade.Compiler.prototype.</span>visitComment (comment)](#apidoc.element.jade.Compiler.prototype.visitComment)
- description and source-code
```javascript
visitComment = function (comment){
  if (!comment.buffer) return;
  if (this.pp) this.prettyIndent(1, true);
  this.buffer('<!--' + comment.val + '-->');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Compiler.prototype.visitDoctype"></a>[function <span class="apidocSignatureSpan">jade.Compiler.prototype.</span>visitDoctype (doctype)](#apidoc.element.jade.Compiler.prototype.visitDoctype)
- description and source-code
```javascript
visitDoctype = function (doctype){
  if (doctype && (doctype.val || !this.doctype)) {
    this.setDoctype(doctype.val || 'default');
  }

  if (this.doctype) this.buffer(this.doctype);
  this.hasCompiledDoctype = true;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Compiler.prototype.visitEach"></a>[function <span class="apidocSignatureSpan">jade.Compiler.prototype.</span>visitEach (each)](#apidoc.element.jade.Compiler.prototype.visitEach)
- description and source-code
```javascript
visitEach = function (each){
  this.buf.push(''
    + '// iterate ' + each.obj + '\n'
    + ';(function(){\n'
    + '  var $$obj = ' + each.obj + ';\n'
    + '  if (\'number\' == typeof $$obj.length) {\n');

  if (each.alternative) {
    this.buf.push('  if ($$obj.length) {');
  }

  this.buf.push(''
    + '    for (var ' + each.key + ' = 0, $$l = $$obj.length; ' + each.key + ' < $$l; ' + each.key + '++) {\n'
    + '      var ' + each.val + ' = $$obj[' + each.key + '];\n');

  this.visit(each.block);

  this.buf.push('    }\n');

  if (each.alternative) {
    this.buf.push('  } else {');
    this.visit(each.alternative);
    this.buf.push('  }');
  }

  this.buf.push(''
    + '  } else {\n'
    + '    var $$l = 0;\n'
    + '    for (var ' + each.key + ' in $$obj) {\n'
    + '      $$l++;'
    + '      var ' + each.val + ' = $$obj[' + each.key + '];\n');

  this.visit(each.block);

  this.buf.push('    }\n');
  if (each.alternative) {
    this.buf.push('    if ($$l === 0) {');
    this.visit(each.alternative);
    this.buf.push('    }');
  }
  this.buf.push('  }\n}).call(this);\n');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Compiler.prototype.visitFilter"></a>[function <span class="apidocSignatureSpan">jade.Compiler.prototype.</span>visitFilter (filter)](#apidoc.element.jade.Compiler.prototype.visitFilter)
- description and source-code
```javascript
visitFilter = function (filter){
  var text = filter.block.nodes.map(
    function(node){ return node.val; }
  ).join('\n');
  filter.attrs.filename = this.options.filename;
  try {
    this.buffer(filters(filter.name, text, filter.attrs), true);
  } catch (err) {
    throw errorAtNode(filter, err);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Compiler.prototype.visitLiteral"></a>[function <span class="apidocSignatureSpan">jade.Compiler.prototype.</span>visitLiteral (node)](#apidoc.element.jade.Compiler.prototype.visitLiteral)
- description and source-code
```javascript
visitLiteral = function (node){
  this.buffer(node.str);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Compiler.prototype.visitMixin"></a>[function <span class="apidocSignatureSpan">jade.Compiler.prototype.</span>visitMixin (mixin)](#apidoc.element.jade.Compiler.prototype.visitMixin)
- description and source-code
```javascript
visitMixin = function (mixin){
  var name = 'jade_mixins[';
  var args = mixin.args || '';
  var block = mixin.block;
  var attrs = mixin.attrs;
  var attrsBlocks = mixin.attributeBlocks.slice();
  var pp = this.pp;
  var dynamic = mixin.name[0]==='#';
  var key = mixin.name;
  if (dynamic) this.dynamicMixins = true;
  name += (dynamic ? mixin.name.substr(2,mixin.name.length-3):'"'+mixin.name+'"')+']';

  this.mixins[key] = this.mixins[key] || {used: false, instances: []};
  if (mixin.call) {
    this.mixins[key].used = true;
    if (pp) this.buf.push("jade_indent.push('" + Array(this.indents + 1).join(pp) + "');")
    if (block || attrs.length || attrsBlocks.length) {

      this.buf.push(name + '.call({');

      if (block) {
        this.buf.push('block: function(){');

        // Render block with no indents, dynamically added when rendered
        this.parentIndents++;
        var _indents = this.indents;
        this.indents = 0;
        this.visit(mixin.block);
        this.indents = _indents;
        this.parentIndents--;

        if (attrs.length || attrsBlocks.length) {
          this.buf.push('},');
        } else {
          this.buf.push('}');
        }
      }

      if (attrsBlocks.length) {
        if (attrs.length) {
          var val = this.attrs(attrs);
          attrsBlocks.unshift(val);
        }
        this.buf.push('attributes: jade.merge([' + attrsBlocks.join(',') + '])');
      } else if (attrs.length) {
        var val = this.attrs(attrs);
        this.buf.push('attributes: ' + val);
      }

      if (args) {
        this.buf.push('}, ' + args + ');');
      } else {
        this.buf.push('});');
      }

    } else {
      this.buf.push(name + '(' + args + ');');
    }
    if (pp) this.buf.push("jade_indent.pop();")
  } else {
    var mixin_start = this.buf.length;
    args = args ? args.split(',') : [];
    var rest;
    if (args.length && /^\.\.\./.test(args[args.length - 1].trim())) {
      rest = args.pop().trim().replace(/^\.\.\./, '');
    }
    // we need use jade_interp here for v8: https://code.google.com/p/v8/issues/detail?id=4165
    // once fixed, use this: this.buf.push(name + ' = function(' + args.join(',') + '){');
    this.buf.push(name + ' = jade_interp = function(' + args.join(',') + '){');
    this.buf.push('var block = (this && this.block), attributes = (this && this.attributes) || {};');
    if (rest) {
      this.buf.push('var ' + rest + ' = [];');
      this.buf.push('for (jade_interp = ' + args.length + '; jade_interp < arguments.length; jade_interp++) {');
      this.buf.push('  ' + rest + '.push(arguments[jade_interp]);');
      this.buf.push('}');
    }
    this.parentIndents++;
    this.visit(block);
    this.parentIndents--;
    this.buf.push('};');
    var mixin_end = this.buf.length;
    this.mixins[key].instances.push({start: mixin_start, end: mixin_end});
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Compiler.prototype.visitMixinBlock"></a>[function <span class="apidocSignatureSpan">jade.Compiler.prototype.</span>visitMixinBlock (block)](#apidoc.element.jade.Compiler.prototype.visitMixinBlock)
- description and source-code
```javascript
visitMixinBlock = function (block){
  if (this.pp) this.buf.push("jade_indent.push('" + Array(this.indents + 1).join(this.pp) + "');");
  this.buf.push('block && block();');
  if (this.pp) this.buf.push("jade_indent.pop();");
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Compiler.prototype.visitNode"></a>[function <span class="apidocSignatureSpan">jade.Compiler.prototype.</span>visitNode (node)](#apidoc.element.jade.Compiler.prototype.visitNode)
- description and source-code
```javascript
visitNode = function (node){
  return this['visit' + node.type](node);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Compiler.prototype.visitTag"></a>[function <span class="apidocSignatureSpan">jade.Compiler.prototype.</span>visitTag (tag)](#apidoc.element.jade.Compiler.prototype.visitTag)
- description and source-code
```javascript
visitTag = function (tag){
  this.indents++;
  var name = tag.name
    , pp = this.pp
    , self = this;

  function bufferName() {
    if (tag.buffer) self.bufferExpression(name);
    else self.buffer(name);
  }

  if ('pre' == tag.name) this.escape = true;

  if (!this.hasCompiledTag) {
    if (!this.hasCompiledDoctype && 'html' == name) {
      this.visitDoctype();
    }
    this.hasCompiledTag = true;
  }

  // pretty print
  if (pp && !tag.isInline())
    this.prettyIndent(0, true);

  if (tag.selfClosing || (!this.xml && selfClosing[tag.name])) {
    this.buffer('<');
    bufferName();
    this.visitAttributes(tag.attrs, tag.attributeBlocks.slice());
    this.terse
      ? this.buffer('>')
      : this.buffer('/>');
    // if it is non-empty throw an error
    if (tag.block &&
        !(tag.block.type === 'Block' && tag.block.nodes.length === 0) &&
        tag.block.nodes.some(function (tag) {
          return tag.type !== 'Text' || !/^\s*$/.test(tag.val)
        })) {
      throw errorAtNode(tag, new Error(name + ' is self closing and should not have content.'));
    }
  } else {
    // Optimize attributes buffering
    this.buffer('<');
    bufferName();
    this.visitAttributes(tag.attrs, tag.attributeBlocks.slice());
    this.buffer('>');
    if (tag.code) this.visitCode(tag.code);
    this.visit(tag.block);

    // pretty print
    if (pp && !tag.isInline() && 'pre' != tag.name && !tag.canInline())
      this.prettyIndent(0, true);

    this.buffer('</');
    bufferName();
    this.buffer('>');
  }

  if ('pre' == tag.name) this.escape = false;

  this.indents--;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Compiler.prototype.visitText"></a>[function <span class="apidocSignatureSpan">jade.Compiler.prototype.</span>visitText (text)](#apidoc.element.jade.Compiler.prototype.visitText)
- description and source-code
```javascript
visitText = function (text){
  this.buffer(text.val, true);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Compiler.prototype.visitWhen"></a>[function <span class="apidocSignatureSpan">jade.Compiler.prototype.</span>visitWhen (node)](#apidoc.element.jade.Compiler.prototype.visitWhen)
- description and source-code
```javascript
visitWhen = function (node){
  if ('default' == node.expr) {
    this.buf.push('default:');
  } else {
    this.buf.push('case ' + node.expr + ':');
  }
  if (node.block) {
    this.visit(node.block);
    this.buf.push('  break;');
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jade.Lexer"></a>[module jade.Lexer](#apidoc.module.jade.Lexer)

#### <a name="apidoc.element.jade.Lexer.Lexer"></a>[function <span class="apidocSignatureSpan">jade.</span>Lexer (str, filename)](#apidoc.element.jade.Lexer.Lexer)
- description and source-code
```javascript
function Lexer(str, filename) {
  this.input = str.replace(/\r\n|\r/g, '\n');
  this.filename = filename;
  this.deferredTokens = [];
  this.lastIndents = 0;
  this.lineno = 1;
  this.stash = [];
  this.indentStack = [];
  this.indentRe = null;
  this.pipeless = false;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jade.Lexer.prototype"></a>[module jade.Lexer.prototype](#apidoc.module.jade.Lexer.prototype)

#### <a name="apidoc.element.jade.Lexer.prototype.advance"></a>[function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>advance ()](#apidoc.element.jade.Lexer.prototype.advance)
- description and source-code
```javascript
advance = function (){
  return this.stashed()
    || this.next();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Lexer.prototype.append"></a>[function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>append ()](#apidoc.element.jade.Lexer.prototype.append)
- description and source-code
```javascript
append = function () {
  var captures;
  if (captures = /^append +([^\n]+)/.exec(this.input)) {
    this.consume(captures[0].length);
    var mode = 'append'
      , name = captures[1]
      , tok = this.tok('block', name);
    tok.mode = mode;
    return tok;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Lexer.prototype.attributesBlock"></a>[function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>attributesBlock ()](#apidoc.element.jade.Lexer.prototype.attributesBlock)
- description and source-code
```javascript
attributesBlock = function () {
  var captures;
  if (/^&attributes\b/.test(this.input)) {
    this.consume(11);
    var args = this.bracketExpression();
    this.consume(args.end + 1);
    return this.tok('&attributes', args.src);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Lexer.prototype.attrs"></a>[function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>attrs ()](#apidoc.element.jade.Lexer.prototype.attrs)
- description and source-code
```javascript
attrs = function () {
  if ('(' == this.input.charAt(0)) {
    var index = this.bracketExpression().end
      , str = this.input.substr(1, index-1)
      , tok = this.tok('attrs');

    assertNestingCorrect(str);

    var quote = '';
    var interpolate = function (attr) {
      return attr.replace(/(\\)?#\{(.+)/g, function(_, escape, expr){
        if (escape) return _;
        try {
          var range = characterParser.parseMax(expr);
          if (expr[range.end] !== '}') return _.substr(0, 2) + interpolate(_.substr(2));
          assertExpression(range.src)
          return quote + " + (" + range.src + ") + " + quote + interpolate(expr.substr(range.end + 1));
        } catch (ex) {
          return _.substr(0, 2) + interpolate(_.substr(2));
        }
      });
    }

    this.consume(index + 1);
    tok.attrs = [];

    var escapedAttr = true
    var key = '';
    var val = '';
    var interpolatable = '';
    var state = characterParser.defaultState();
    var loc = 'key';
    var isEndOfAttribute = function (i) {
      if (key.trim() === '') return false;
      if (i === str.length) return true;
      if (loc === 'key') {
        if (str[i] === ' ' || str[i] === '\n') {
          for (var x = i; x < str.length; x++) {
            if (str[x] != ' ' && str[x] != '\n') {
              if (str[x] === '=' || str[x] === '!' || str[x] === ',') return false;
              else return true;
            }
          }
        }
        return str[i] === ','
      } else if (loc === 'value' && !state.isNesting()) {
        try {
          assertExpression(val);
          if (str[i] === ' ' || str[i] === '\n') {
            for (var x = i; x < str.length; x++) {
              if (str[x] != ' ' && str[x] != '\n') {
                if (characterParser.isPunctuator(str[x]) && str[x] != '"' && str[x] != "'") return false;
                else return true;
              }
            }
          }
          return str[i] === ',';
        } catch (ex) {
          return false;
        }
      }
    }

    this.lineno += str.split("\n").length - 1;

    for (var i = 0; i <= str.length; i++) {
      if (isEndOfAttribute(i)) {
        val = val.trim();
        if (val) assertExpression(val)
        key = key.trim();
        key = key.replace(/^['"]|['"]$/g, '');
        tok.attrs.push({
          name: key,
          val: '' == val ? true : val,
          escaped: escapedAttr
        });
        key = val = '';
        loc = 'key';
        escapedAttr = false;
      } else {
        switch (loc) {
          case 'key-char':
            if (str[i] === quote) {
              loc = 'key';
              if (i + 1 < str.length && [' ', ',', '!', '=', '\n'].indexOf(str[i + 1]) === -1)
                throw new Error('Unexpected character ' + str[i + 1] + ' expected ' ', '\\n', ',', '!' or '='');
            } else {
              key += str[i];
            }
            break;
          case 'key':
            if (key === '' && (str[i] === '"' || str[i] === "'")) {
              loc = 'key-char';
              quote = str[i];
            } else if (str[i] === '!' || str[i] === '=') {
              escapedAttr = str[i] !== '!';
              if (str[i] === '!') i++;
              if (str[i] !== '=') throw new Error('Unexpected character ' + str[i] + ' expected '='');
              loc = 'value';
              state = characterParser.defaultState();
            } else {
              key += str[i]
            }
            break;
          case 'value':
            state = characterParser.parseChar(str[i], state);
            if (state.isString()) {
              loc = 'string';
              quote = str[i];
              interpolatable = str[i];
            } else {
              val += str[i];
            }
            break;
          case 'string':
            state = characterParser.parseChar(str[i], state);
            interpolatable += str[i];
            if (!state.isString()) {
              loc = 'value';
              val += interpolate(interpolatable);
            }
            break;
        }
      }
    }

    if ('/' == this.input.char ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Lexer.prototype.blank"></a>[function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>blank ()](#apidoc.element.jade.Lexer.prototype.blank)
- description and source-code
```javascript
blank = function () {
  var captures;
  if (captures = /^\n *\n/.exec(this.input)) {
    this.consume(captures[0].length - 1);
    ++this.lineno;
    if (this.pipeless) return this.tok('text', '');
    return this.next();
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Lexer.prototype.block"></a>[function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>block ()](#apidoc.element.jade.Lexer.prototype.block)
- description and source-code
```javascript
block = function () {
  var captures;
  if (captures = /^block\b *(?:(prepend|append) +)?([^\n]+)/.exec(this.input)) {
    this.consume(captures[0].length);
    var mode = captures[1] || 'replace'
      , name = captures[2]
      , tok = this.tok('block', name);

    tok.mode = mode;
    return tok;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Lexer.prototype.blockCode"></a>[function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>blockCode ()](#apidoc.element.jade.Lexer.prototype.blockCode)
- description and source-code
```javascript
blockCode = function () {
  var captures;
  if (captures = /^-\n/.exec(this.input)) {
    this.consume(captures[0].length - 1);
    var tok = this.tok('blockCode');
    this.pipeless = true;
    return tok;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Lexer.prototype.bracketExpression"></a>[function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>bracketExpression (skip)](#apidoc.element.jade.Lexer.prototype.bracketExpression)
- description and source-code
```javascript
bracketExpression = function (skip){
  skip = skip || 0;
  var start = this.input[skip];
  if (start != '(' && start != '{' && start != '[') throw new Error('unrecognized start character');
  var end = ({'(': ')', '{': '}', '[': ']'})[start];
  var range = characterParser.parseMax(this.input, {start: skip + 1});
  if (this.input[range.end] !== end) throw new Error('start character ' + start + ' does not match end character ' + this.input[
range.end]);
  return range;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Lexer.prototype.call"></a>[function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>call ()](#apidoc.element.jade.Lexer.prototype.call)
- description and source-code
```javascript
call = function (){

  var tok, captures;
  if (captures = /^\+(\s*)(([-\w]+)|(#\{))/.exec(this.input)) {
    // try to consume simple or interpolated call
    if (captures[3]) {
      // simple call
      this.consume(captures[0].length);
      tok = this.tok('call', captures[3]);
    } else {
      // interpolated call
      var match = this.bracketExpression(2 + captures[1].length);
      this.consume(match.end + 1);
      assertExpression(match.src);
      tok = this.tok('call', '#{'+match.src+'}');
    }

    // Check for args (not attributes)
    if (captures = /^ *\(/.exec(this.input)) {
      var range = this.bracketExpression(captures[0].length - 1);
      if (!/^\s*[-\w]+ *=/.test(range.src)) { // not attributes
        this.consume(range.end + 1);
        tok.args = range.src;
      }
      if (tok.args) {
        assertExpression('[' + tok.args + ']');
      }
    }

    return tok;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Lexer.prototype.case"></a>[function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>case ()](#apidoc.element.jade.Lexer.prototype.case)
- description and source-code
```javascript
case = function () {
  return this.scan(/^case +([^\n]+)/, 'case');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Lexer.prototype.className"></a>[function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>className ()](#apidoc.element.jade.Lexer.prototype.className)
- description and source-code
```javascript
className = function () {
  return this.scan(/^\.([\w-]+)/, 'class');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Lexer.prototype.code"></a>[function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>code ()](#apidoc.element.jade.Lexer.prototype.code)
- description and source-code
```javascript
code = function () {
  var captures;
  if (captures = /^(!?=|-)[ \t]*([^\n]+)/.exec(this.input)) {
    this.consume(captures[0].length);
    var flags = captures[1];
    captures[1] = captures[2];
    var tok = this.tok('code', captures[1]);
    tok.escape = flags.charAt(0) === '=';
    tok.buffer = flags.charAt(0) === '=' || flags.charAt(1) === '=';
    if (tok.buffer) assertExpression(captures[1])
    return tok;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Lexer.prototype.colon"></a>[function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>colon ()](#apidoc.element.jade.Lexer.prototype.colon)
- description and source-code
```javascript
colon = function () {
  var good = /^: +/.test(this.input);
  var res = this.scan(/^: */, ':');
  if (res && !good) {
    console.warn('Warning: space required after ':' on line ' + this.lineno +
        ' of jade file "' + this.filename + '"');
  }
  return res;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Lexer.prototype.comment"></a>[function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>comment ()](#apidoc.element.jade.Lexer.prototype.comment)
- description and source-code
```javascript
comment = function () {
  var captures;
  if (captures = /^\/\/(-)?([^\n]*)/.exec(this.input)) {
    this.consume(captures[0].length);
    var tok = this.tok('comment', captures[2]);
    tok.buffer = '-' != captures[1];
    this.pipeless = true;
    return tok;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Lexer.prototype.conditional"></a>[function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>conditional ()](#apidoc.element.jade.Lexer.prototype.conditional)
- description and source-code
```javascript
conditional = function () {
  var captures;
  if (captures = /^(if|unless|else if|else)\b([^\n]*)/.exec(this.input)) {
    this.consume(captures[0].length);
    var type = captures[1]
    var js = captures[2];
    var isIf = false;
    var isElse = false;

    switch (type) {
      case 'if':
        assertExpression(js)
        js = 'if (' + js + ')';
        isIf = true;
        break;
      case 'unless':
        assertExpression(js)
        js = 'if (!(' + js + '))';
        isIf = true;
        break;
      case 'else if':
        assertExpression(js)
        js = 'else if (' + js + ')';
        isIf = true;
        isElse = true;
        break;
      case 'else':
        if (js && js.trim()) {
          throw new Error(''else' cannot have a condition, perhaps you meant 'else if'');
        }
        js = 'else';
        isElse = true;
        break;
    }
    var tok = this.tok('code', js);
    tok.isElse = isElse;
    tok.isIf = isIf;
    tok.requiresBlock = true;
    return tok;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Lexer.prototype.consume"></a>[function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>consume (len)](#apidoc.element.jade.Lexer.prototype.consume)
- description and source-code
```javascript
consume = function (len){
  this.input = this.input.substr(len);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Lexer.prototype.default"></a>[function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>default ()](#apidoc.element.jade.Lexer.prototype.default)
- description and source-code
```javascript
default = function () {
  return this.scan(/^default */, 'default');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Lexer.prototype.defer"></a>[function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>defer (tok)](#apidoc.element.jade.Lexer.prototype.defer)
- description and source-code
```javascript
defer = function (tok){
  this.deferredTokens.push(tok);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Lexer.prototype.deferred"></a>[function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>deferred ()](#apidoc.element.jade.Lexer.prototype.deferred)
- description and source-code
```javascript
deferred = function () {
  return this.deferredTokens.length
    && this.deferredTokens.shift();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Lexer.prototype.doctype"></a>[function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>doctype ()](#apidoc.element.jade.Lexer.prototype.doctype)
- description and source-code
```javascript
doctype = function () {
  if (this.scan(/^!!! *([^\n]+)?/, 'doctype')) {
    throw new Error(''!!!' is deprecated, you must now use 'doctype'');
  }
  var node = this.scan(/^(?:doctype) *([^\n]+)?/, 'doctype');
  if (node && node.val && node.val.trim() === '5') {
    throw new Error(''doctype 5' is deprecated, you must now use 'doctype html'');
  }
  return node;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Lexer.prototype.dot"></a>[function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>dot ()](#apidoc.element.jade.Lexer.prototype.dot)
- description and source-code
```javascript
dot = function () {
  var match;
  if (match = this.scan(/^\./, 'dot')) {
    this.pipeless = true;
    return match;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Lexer.prototype.each"></a>[function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>each ()](#apidoc.element.jade.Lexer.prototype.each)
- description and source-code
```javascript
each = function () {
  var captures;
  if (captures = /^(?:- *)?(?:each|for) +([a-zA-Z_$][\w$]*)(?: *, *([a-zA-Z_$][\w$]*))? * in *([^\n]+)/.exec(this.input)) {
    this.consume(captures[0].length);
    var tok = this.tok('each', captures[1]);
    tok.key = captures[2] || '$index';
    assertExpression(captures[3])
    tok.code = captures[3];
    return tok;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Lexer.prototype.eos"></a>[function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>eos ()](#apidoc.element.jade.Lexer.prototype.eos)
- description and source-code
```javascript
eos = function () {
  if (this.input.length) return;
  if (this.indentStack.length) {
    this.indentStack.shift();
    return this.tok('outdent');
  } else {
    return this.tok('eos');
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Lexer.prototype.extends"></a>[function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>extends ()](#apidoc.element.jade.Lexer.prototype.extends)
- description and source-code
```javascript
extends = function () {
  return this.scan(/^extends? +([^\n]+)/, 'extends');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Lexer.prototype.fail"></a>[function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>fail ()](#apidoc.element.jade.Lexer.prototype.fail)
- description and source-code
```javascript
fail = function () {
  throw new Error('unexpected text ' + this.input.substr(0, 5));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Lexer.prototype.filter"></a>[function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>filter ()](#apidoc.element.jade.Lexer.prototype.filter)
- description and source-code
```javascript
filter = function () {
  var tok = this.scan(/^:([\w\-]+)/, 'filter');
  if (tok) {
    this.pipeless = true;
    return tok;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Lexer.prototype.id"></a>[function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>id ()](#apidoc.element.jade.Lexer.prototype.id)
- description and source-code
```javascript
id = function () {
  return this.scan(/^#([\w-]+)/, 'id');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Lexer.prototype.include"></a>[function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>include ()](#apidoc.element.jade.Lexer.prototype.include)
- description and source-code
```javascript
include = function () {
  return this.scan(/^include +([^\n]+)/, 'include');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Lexer.prototype.includeFiltered"></a>[function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>includeFiltered ()](#apidoc.element.jade.Lexer.prototype.includeFiltered)
- description and source-code
```javascript
includeFiltered = function () {
  var captures;
  if (captures = /^include:([\w\-]+)([\( ])/.exec(this.input)) {
    this.consume(captures[0].length - 1);
    var filter = captures[1];
    var attrs = captures[2] === '(' ? this.attrs() : null;
    if (!(captures[2] === ' ' || this.input[0] === ' ')) {
      throw new Error('expected space after include:filter but got ' + utils.stringify(this.input[0]));
    }
    captures = /^ *([^\n]+)/.exec(this.input);
    if (!captures || captures[1].trim() === '') {
      throw new Error('missing path for include:filter');
    }
    this.consume(captures[0].length);
    var path = captures[1];
    var tok = this.tok('include', path);
    tok.filter = filter;
    tok.attrs = attrs;
    return tok;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Lexer.prototype.indent"></a>[function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>indent ()](#apidoc.element.jade.Lexer.prototype.indent)
- description and source-code
```javascript
indent = function () {
  var captures, re;

  // established regexp
  if (this.indentRe) {
    captures = this.indentRe.exec(this.input);
  // determine regexp
  } else {
    // tabs
    re = /^\n(\t*) */;
    captures = re.exec(this.input);

    // spaces
    if (captures && !captures[1].length) {
      re = /^\n( *)/;
      captures = re.exec(this.input);
    }

    // established
    if (captures && captures[1].length) this.indentRe = re;
  }

  if (captures) {
    var tok
      , indents = captures[1].length;

    ++this.lineno;
    this.consume(indents + 1);

    if (' ' == this.input[0] || '\t' == this.input[0]) {
      throw new Error('Invalid indentation, you can use tabs or spaces but not both');
    }

    // blank line
    if ('\n' == this.input[0]) {
      this.pipeless = false;
      return this.tok('newline');
    }

    // outdent
    if (this.indentStack.length && indents < this.indentStack[0]) {
      while (this.indentStack.length && this.indentStack[0] > indents) {
        this.stash.push(this.tok('outdent'));
        this.indentStack.shift();
      }
      tok = this.stash.pop();
    // indent
    } else if (indents && indents != this.indentStack[0]) {
      this.indentStack.unshift(indents);
      tok = this.tok('indent', indents);
    // newline
    } else {
      tok = this.tok('newline');
    }

    this.pipeless = false;
    return tok;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Lexer.prototype.interpolation"></a>[function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>interpolation ()](#apidoc.element.jade.Lexer.prototype.interpolation)
- description and source-code
```javascript
interpolation = function () {
  if (/^#\{/.test(this.input)) {
    var match = this.bracketExpression(1);

    this.consume(match.end + 1);
    return this.tok('interpolation', match.src);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Lexer.prototype.lookahead"></a>[function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>lookahead (n)](#apidoc.element.jade.Lexer.prototype.lookahead)
- description and source-code
```javascript
lookahead = function (n){
  var fetch = n - this.stash.length;
  while (fetch-- > 0) this.stash.push(this.next());
  return this.stash[--n];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Lexer.prototype.mixin"></a>[function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>mixin ()](#apidoc.element.jade.Lexer.prototype.mixin)
- description and source-code
```javascript
mixin = function (){
  var captures;
  if (captures = /^mixin +([-\w]+)(?: *\((.*)\))? */.exec(this.input)) {
    this.consume(captures[0].length);
    var tok = this.tok('mixin', captures[1]);
    tok.args = captures[2];
    return tok;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Lexer.prototype.mixinBlock"></a>[function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>mixinBlock ()](#apidoc.element.jade.Lexer.prototype.mixinBlock)
- description and source-code
```javascript
mixinBlock = function () {
  var captures;
  if (captures = /^block[ \t]*(\n|$)/.exec(this.input)) {
    this.consume(captures[0].length - captures[1].length);
    return this.tok('mixin-block');
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Lexer.prototype.next"></a>[function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>next ()](#apidoc.element.jade.Lexer.prototype.next)
- description and source-code
```javascript
next = function () {
  return this.deferred()
    || this.blank()
    || this.eos()
    || this.pipelessText()
    || this.yield()
    || this.doctype()
    || this.interpolation()
    || this["case"]()
    || this.when()
    || this["default"]()
    || this["extends"]()
    || this.append()
    || this.prepend()
    || this.block()
    || this.mixinBlock()
    || this.include()
    || this.includeFiltered()
    || this.mixin()
    || this.call()
    || this.conditional()
    || this.each()
    || this["while"]()
    || this.tag()
    || this.filter()
    || this.blockCode()
    || this.code()
    || this.id()
    || this.className()
    || this.attrs()
    || this.attributesBlock()
    || this.indent()
    || this.text()
    || this.comment()
    || this.colon()
    || this.dot()
    || this.textFail()
    || this.fail();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Lexer.prototype.pipelessText"></a>[function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>pipelessText ()](#apidoc.element.jade.Lexer.prototype.pipelessText)
- description and source-code
```javascript
pipelessText = function () {
  if (!this.pipeless) return;
  var captures, re;

  // established regexp
  if (this.indentRe) {
    captures = this.indentRe.exec(this.input);
  // determine regexp
  } else {
    // tabs
    re = /^\n(\t*) */;
    captures = re.exec(this.input);

    // spaces
    if (captures && !captures[1].length) {
      re = /^\n( *)/;
      captures = re.exec(this.input);
    }

    // established
    if (captures && captures[1].length) this.indentRe = re;
  }

  var indents = captures && captures[1].length;
  if (indents && (this.indentStack.length === 0 || indents > this.indentStack[0])) {
    var indent = captures[1];
    var line;
    var tokens = [];
    var isMatch;
    do {
      // text has '\n' as a prefix
      var i = this.input.substr(1).indexOf('\n');
      if (-1 == i) i = this.input.length - 1;
      var str = this.input.substr(1, i);
      isMatch = str.substr(0, indent.length) === indent || !str.trim();
      if (isMatch) {
        // consume test along with '\n' prefix if match
        this.consume(str.length + 1);
        ++this.lineno;
        tokens.push(str.substr(indent.length));
      }
    } while(this.input.length && isMatch);
    while (this.input.length === 0 && tokens[tokens.length - 1] === '') tokens.pop();
    return this.tok('pipeless-text', tokens);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Lexer.prototype.prepend"></a>[function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>prepend ()](#apidoc.element.jade.Lexer.prototype.prepend)
- description and source-code
```javascript
prepend = function () {
  var captures;
  if (captures = /^prepend +([^\n]+)/.exec(this.input)) {
    this.consume(captures[0].length);
    var mode = 'prepend'
      , name = captures[1]
      , tok = this.tok('block', name);
    tok.mode = mode;
    return tok;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Lexer.prototype.scan"></a>[function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>scan (regexp, type)](#apidoc.element.jade.Lexer.prototype.scan)
- description and source-code
```javascript
scan = function (regexp, type){
  var captures;
  if (captures = regexp.exec(this.input)) {
    this.consume(captures[0].length);
    return this.tok(type, captures[1]);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Lexer.prototype.stashed"></a>[function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>stashed ()](#apidoc.element.jade.Lexer.prototype.stashed)
- description and source-code
```javascript
stashed = function () {
  return this.stash.length
    && this.stash.shift();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Lexer.prototype.tag"></a>[function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>tag ()](#apidoc.element.jade.Lexer.prototype.tag)
- description and source-code
```javascript
tag = function () {
  var captures;
  if (captures = /^(\w[-:\w]*)(\/?)/.exec(this.input)) {
    this.consume(captures[0].length);
    var tok, name = captures[1];
    if (':' == name[name.length - 1]) {
      name = name.slice(0, -1);
      tok = this.tok('tag', name);
      this.defer(this.tok(':'));
      if (this.input[0] !== ' ') {
        console.warn('Warning: space required after ':' on line ' + this.lineno +
            ' of jade file "' + this.filename + '"');
      }
      while (' ' == this.input[0]) this.input = this.input.substr(1);
    } else {
      tok = this.tok('tag', name);
    }
    tok.selfClosing = !!captures[2];
    return tok;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Lexer.prototype.text"></a>[function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>text ()](#apidoc.element.jade.Lexer.prototype.text)
- description and source-code
```javascript
text = function () {
  return this.scan(/^(?:\| ?| )([^\n]+)/, 'text') ||
    this.scan(/^\|?( )/, 'text') ||
    this.scan(/^(<[^\n]*)/, 'text');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Lexer.prototype.textFail"></a>[function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>textFail ()](#apidoc.element.jade.Lexer.prototype.textFail)
- description and source-code
```javascript
textFail = function () {
  var tok;
  if (tok = this.scan(/^([^\.\n][^\n]+)/, 'text')) {
    console.warn('Warning: missing space before text for line ' + this.lineno +
        ' of jade file "' + this.filename + '"');
    return tok;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Lexer.prototype.tok"></a>[function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>tok (type, val)](#apidoc.element.jade.Lexer.prototype.tok)
- description and source-code
```javascript
tok = function (type, val){
  return {
      type: type
    , line: this.lineno
    , val: val
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Lexer.prototype.when"></a>[function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>when ()](#apidoc.element.jade.Lexer.prototype.when)
- description and source-code
```javascript
when = function () {
  return this.scan(/^when +([^:\n]+)/, 'when');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Lexer.prototype.while"></a>[function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>while ()](#apidoc.element.jade.Lexer.prototype.while)
- description and source-code
```javascript
while = function () {
  var captures;
  if (captures = /^while +([^\n]+)/.exec(this.input)) {
    this.consume(captures[0].length);
    assertExpression(captures[1])
    var tok = this.tok('code', 'while (' + captures[1] + ')');
    tok.requiresBlock = true;
    return tok;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Lexer.prototype.yield"></a>[function <span class="apidocSignatureSpan">jade.Lexer.prototype.</span>yield ()](#apidoc.element.jade.Lexer.prototype.yield)
- description and source-code
```javascript
yield = function () {
  return this.scan(/^yield */, 'yield');
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jade.Parser"></a>[module jade.Parser](#apidoc.module.jade.Parser)

#### <a name="apidoc.element.jade.Parser.Parser"></a>[function <span class="apidocSignatureSpan">jade.</span>Parser (str, filename, options)](#apidoc.element.jade.Parser.Parser)
- description and source-code
```javascript
function Parser(str, filename, options){
  //Strip any UTF-8 BOM off of the start of 'str', if it exists.
  this.input = str.replace(/^\uFEFF/, '');
  this.lexer = new Lexer(this.input, filename);
  this.filename = filename;
  this.blocks = {};
  this.mixins = {};
  this.options = options;
  this.contexts = [this];
  this.inMixin = 0;
  this.dependencies = [];
  this.inBlock = 0;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jade.Parser.prototype"></a>[module jade.Parser.prototype](#apidoc.module.jade.Parser.prototype)

#### <a name="apidoc.element.jade.Parser.prototype.accept"></a>[function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>accept (type)](#apidoc.element.jade.Parser.prototype.accept)
- description and source-code
```javascript
accept = function (type){
  if (this.peek().type === type) {
    return this.advance();
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Parser.prototype.advance"></a>[function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>advance ()](#apidoc.element.jade.Parser.prototype.advance)
- description and source-code
```javascript
advance = function (){
  return this.lexer.advance();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Parser.prototype.block"></a>[function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>block ()](#apidoc.element.jade.Parser.prototype.block)
- description and source-code
```javascript
block = function (){
  var block = new nodes.Block;
  block.line = this.line();
  block.filename = this.filename;
  this.expect('indent');
  while ('outdent' != this.peek().type) {
    if ('newline' == this.peek().type) {
      this.advance();
    } else {
      var expr = this.parseExpr();
      expr.filename = this.filename;
      block.push(expr);
    }
  }
  this.expect('outdent');
  return block;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Parser.prototype.constructor"></a>[function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>constructor (str, filename, options)](#apidoc.element.jade.Parser.prototype.constructor)
- description and source-code
```javascript
function Parser(str, filename, options){
  //Strip any UTF-8 BOM off of the start of 'str', if it exists.
  this.input = str.replace(/^\uFEFF/, '');
  this.lexer = new Lexer(this.input, filename);
  this.filename = filename;
  this.blocks = {};
  this.mixins = {};
  this.options = options;
  this.contexts = [this];
  this.inMixin = 0;
  this.dependencies = [];
  this.inBlock = 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Parser.prototype.context"></a>[function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>context (parser)](#apidoc.element.jade.Parser.prototype.context)
- description and source-code
```javascript
context = function (parser){
  if (parser) {
    this.contexts.push(parser);
  } else {
    return this.contexts.pop();
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Parser.prototype.expect"></a>[function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>expect (type)](#apidoc.element.jade.Parser.prototype.expect)
- description and source-code
```javascript
expect = function (type){
  if (this.peek().type === type) {
    return this.advance();
  } else {
    throw new Error('expected "' + type + '", but got "' + this.peek().type + '"');
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Parser.prototype.line"></a>[function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>line ()](#apidoc.element.jade.Parser.prototype.line)
- description and source-code
```javascript
line = function () {
  return this.lexer.lineno;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Parser.prototype.lookahead"></a>[function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>lookahead (n)](#apidoc.element.jade.Parser.prototype.lookahead)
- description and source-code
```javascript
lookahead = function (n){
  return this.lexer.lookahead(n);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Parser.prototype.parse"></a>[function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>parse ()](#apidoc.element.jade.Parser.prototype.parse)
- description and source-code
```javascript
parse = function (){
  var block = new nodes.Block, parser;
  block.line = 0;
  block.filename = this.filename;

  while ('eos' != this.peek().type) {
    if ('newline' == this.peek().type) {
      this.advance();
    } else {
      var next = this.peek();
      var expr = this.parseExpr();
      expr.filename = expr.filename || this.filename;
      expr.line = next.line;
      block.push(expr);
    }
  }

  if (parser = this.extending) {
    this.context(parser);
    var ast = parser.parse();
    this.context();

    // hoist mixins
    for (var name in this.mixins)
      ast.unshift(this.mixins[name]);
    return ast;
  }

  if (!this.extending && !this.included && Object.keys(this.blocks).length){
    var blocks = [];
    utils.walkAST(block, function (node) {
      if (node.type === 'Block' && node.name) {
        blocks.push(node.name);
      }
    });
    Object.keys(this.blocks).forEach(function (name) {
      if (blocks.indexOf(name) === -1 && !this.blocks[name].isSubBlock) {
        console.warn('Warning: Unexpected block "'
                     + name
                     + '" '
                     + ' on line '
                     + this.blocks[name].line
                     + ' of '
                     + (this.blocks[name].filename)
                     + '. This block is never used. This warning will be an error in v2.0.0');
      }
    }.bind(this));
  }

  return block;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Parser.prototype.parseBlock"></a>[function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>parseBlock ()](#apidoc.element.jade.Parser.prototype.parseBlock)
- description and source-code
```javascript
parseBlock = function (){
  var block = this.expect('block');
  var mode = block.mode;
  var name = block.val.trim();

  var line = block.line;

  this.inBlock++;
  block = 'indent' == this.peek().type
    ? this.block()
    : new nodes.Block(new nodes.Literal(''));
  this.inBlock--;
  block.name = name;
  block.line = line;

  var prev = this.blocks[name] || {prepended: [], appended: []}
  if (prev.mode === 'replace') return this.blocks[name] = prev;

  var allNodes = prev.prepended.concat(block.nodes).concat(prev.appended);

  switch (mode) {
    case 'append':
      prev.appended = prev.parser === this ?
                      prev.appended.concat(block.nodes) :
                      block.nodes.concat(prev.appended);
      break;
    case 'prepend':
      prev.prepended = prev.parser === this ?
                       block.nodes.concat(prev.prepended) :
                       prev.prepended.concat(block.nodes);
      break;
  }
  block.nodes = allNodes;
  block.appended = prev.appended;
  block.prepended = prev.prepended;
  block.mode = mode;
  block.parser = this;

  block.isSubBlock = this.inBlock > 0;

  return this.blocks[name] = block;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Parser.prototype.parseBlockCode"></a>[function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>parseBlockCode ()](#apidoc.element.jade.Parser.prototype.parseBlockCode)
- description and source-code
```javascript
parseBlockCode = function (){
  var tok = this.expect('blockCode');
  var node;
  var body = this.peek();
  var text;
  if (body.type === 'pipeless-text') {
    this.advance();
    text = body.val.join('\n');
  } else {
    text = '';
  }
    node = new nodes.Code(text, false, false);
    return node;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Parser.prototype.parseBlockExpansion"></a>[function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>parseBlockExpansion ()](#apidoc.element.jade.Parser.prototype.parseBlockExpansion)
- description and source-code
```javascript
parseBlockExpansion = function (){
  if (':' == this.peek().type) {
    this.advance();
    return new nodes.Block(this.parseExpr());
  } else {
    return this.block();
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Parser.prototype.parseCall"></a>[function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>parseCall ()](#apidoc.element.jade.Parser.prototype.parseCall)
- description and source-code
```javascript
parseCall = function (){
  var tok = this.expect('call');
  var name = tok.val;
  var args = tok.args;
  var mixin = new nodes.Mixin(name, args, new nodes.Block, true);

  this.tag(mixin);
  if (mixin.code) {
    mixin.block.push(mixin.code);
    mixin.code = null;
  }
  if (mixin.block.isEmpty()) mixin.block = null;
  return mixin;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Parser.prototype.parseCase"></a>[function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>parseCase ()](#apidoc.element.jade.Parser.prototype.parseCase)
- description and source-code
```javascript
parseCase = function (){
  var val = this.expect('case').val;
  var node = new nodes.Case(val);
  node.line = this.line();

  var block = new nodes.Block;
  block.line = this.line();
  block.filename = this.filename;
  this.expect('indent');
  while ('outdent' != this.peek().type) {
    switch (this.peek().type) {
      case 'comment':
      case 'newline':
        this.advance();
        break;
      case 'when':
        block.push(this.parseWhen());
        break;
      case 'default':
        block.push(this.parseDefault());
        break;
      default:
        throw new Error('Unexpected token "' + this.peek().type
                        + '", expected "when", "default" or "newline"');
    }
  }
  this.expect('outdent');

  node.block = block;

  return node;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Parser.prototype.parseCode"></a>[function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>parseCode (afterIf)](#apidoc.element.jade.Parser.prototype.parseCode)
- description and source-code
```javascript
parseCode = function (afterIf){
  var tok = this.expect('code');
  var node = new nodes.Code(tok.val, tok.buffer, tok.escape);
  var block;
  node.line = this.line();

  // throw an error if an else does not have an if
  if (tok.isElse && !tok.hasIf) {
    throw new Error('Unexpected else without if');
  }

  // handle block
  block = 'indent' == this.peek().type;
  if (block) {
    node.block = this.block();
  }

  // handle missing block
  if (tok.requiresBlock && !block) {
    node.block = new nodes.Block();
  }

  // mark presense of if for future elses
  if (tok.isIf && this.peek().isElse) {
    this.peek().hasIf = true;
  } else if (tok.isIf && this.peek().type === 'newline' && this.lookahead(2).isElse) {
    this.lookahead(2).hasIf = true;
  }

  return node;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Parser.prototype.parseComment"></a>[function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>parseComment ()](#apidoc.element.jade.Parser.prototype.parseComment)
- description and source-code
```javascript
parseComment = function (){
  var tok = this.expect('comment');
  var node;

  var block;
  if (block = this.parseTextBlock()) {
    node = new nodes.BlockComment(tok.val, block, tok.buffer);
  } else {
    node = new nodes.Comment(tok.val, tok.buffer);
  }

  node.line = this.line();
  return node;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Parser.prototype.parseDefault"></a>[function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>parseDefault ()](#apidoc.element.jade.Parser.prototype.parseDefault)
- description and source-code
```javascript
parseDefault = function (){
  this.expect('default');
  return new nodes.Case.When('default', this.parseBlockExpansion());
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Parser.prototype.parseDoctype"></a>[function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>parseDoctype ()](#apidoc.element.jade.Parser.prototype.parseDoctype)
- description and source-code
```javascript
parseDoctype = function (){
  var tok = this.expect('doctype');
  var node = new nodes.Doctype(tok.val);
  node.line = this.line();
  return node;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Parser.prototype.parseEach"></a>[function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>parseEach ()](#apidoc.element.jade.Parser.prototype.parseEach)
- description and source-code
```javascript
parseEach = function (){
  var tok = this.expect('each');
  var node = new nodes.Each(tok.code, tok.val, tok.key);
  node.line = this.line();
  node.block = this.block();
  if (this.peek().type == 'code' && this.peek().val == 'else') {
    this.advance();
    node.alternative = this.block();
  }
  return node;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Parser.prototype.parseExpr"></a>[function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>parseExpr ()](#apidoc.element.jade.Parser.prototype.parseExpr)
- description and source-code
```javascript
parseExpr = function (){
  switch (this.peek().type) {
    case 'tag':
      return this.parseTag();
    case 'mixin':
      return this.parseMixin();
    case 'block':
      return this.parseBlock();
    case 'mixin-block':
      return this.parseMixinBlock();
    case 'case':
      return this.parseCase();
    case 'extends':
      return this.parseExtends();
    case 'include':
      return this.parseInclude();
    case 'doctype':
      return this.parseDoctype();
    case 'filter':
      return this.parseFilter();
    case 'comment':
      return this.parseComment();
    case 'text':
      return this.parseText();
    case 'each':
      return this.parseEach();
    case 'code':
      return this.parseCode();
    case 'blockCode':
      return this.parseBlockCode();
    case 'call':
      return this.parseCall();
    case 'interpolation':
      return this.parseInterpolation();
    case 'yield':
      this.advance();
      var block = new nodes.Block;
      block.yield = true;
      return block;
    case 'id':
    case 'class':
      var tok = this.advance();
      this.lexer.defer(this.lexer.tok('tag', 'div'));
      this.lexer.defer(tok);
      return this.parseExpr();
    default:
      throw new Error('unexpected token "' + this.peek().type + '"');
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Parser.prototype.parseExtends"></a>[function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>parseExtends ()](#apidoc.element.jade.Parser.prototype.parseExtends)
- description and source-code
```javascript
parseExtends = function (){
  var fs = require('fs');

  var path = this.resolvePath(this.expect('extends').val.trim(), 'extends');
  if ('.jade' != path.substr(-5)) path += '.jade';

  this.dependencies.push(path);
  var str = fs.readFileSync(path, 'utf8');
  var parser = new this.constructor(str, path, this.options);
  parser.dependencies = this.dependencies;

  parser.blocks = this.blocks;
  parser.included = this.included;
  parser.contexts = this.contexts;
  this.extending = parser;

  // TODO: null node
  return new nodes.Literal('');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Parser.prototype.parseFilter"></a>[function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>parseFilter ()](#apidoc.element.jade.Parser.prototype.parseFilter)
- description and source-code
```javascript
parseFilter = function (){
  var tok = this.expect('filter');
  var attrs = this.accept('attrs');
  var block;

  block = this.parseTextBlock() || new nodes.Block();

  var options = {};
  if (attrs) {
    attrs.attrs.forEach(function (attribute) {
      options[attribute.name] = constantinople.toConstant(attribute.val);
    });
  }

  var node = new nodes.Filter(tok.val, block, options);
  node.line = this.line();
  return node;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Parser.prototype.parseInclude"></a>[function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>parseInclude ()](#apidoc.element.jade.Parser.prototype.parseInclude)
- description and source-code
```javascript
parseInclude = function (){
  var fs = require('fs');
  var tok = this.expect('include');

  var path = this.resolvePath(tok.val.trim(), 'include');
  this.dependencies.push(path);
  // has-filter
  if (tok.filter) {
    var str = fs.readFileSync(path, 'utf8').replace(/\r/g, '');
    var options = {filename: path};
    if (tok.attrs) {
      tok.attrs.attrs.forEach(function (attribute) {
        options[attribute.name] = constantinople.toConstant(attribute.val);
      });
    }
    str = filters(tok.filter, str, options);
    return new nodes.Literal(str);
  }

  // non-jade
  if ('.jade' != path.substr(-5)) {
    var str = fs.readFileSync(path, 'utf8').replace(/\r/g, '');
    return new nodes.Literal(str);
  }

  var str = fs.readFileSync(path, 'utf8');
  var parser = new this.constructor(str, path, this.options);
  parser.dependencies = this.dependencies;

  parser.blocks = utils.merge({}, this.blocks);
  parser.included = true;

  parser.mixins = this.mixins;

  this.context(parser);
  var ast = parser.parse();
  this.context();
  ast.filename = path;

  if ('indent' == this.peek().type) {
    ast.includeBlock().push(this.block());
  }

  return ast;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Parser.prototype.parseInlineTagsInText"></a>[function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>parseInlineTagsInText (str)](#apidoc.element.jade.Parser.prototype.parseInlineTagsInText)
- description and source-code
```javascript
parseInlineTagsInText = function (str) {
  var line = this.line();

  var match = /(\\)?#\[((?:.|\n)*)$/.exec(str);
  if (match) {
    if (match[1]) { // escape
      var text = new nodes.Text(str.substr(0, match.index) + '#[');
      text.line = line;
      var rest = this.parseInlineTagsInText(match[2]);
      if (rest[0].type === 'Text') {
        text.val += rest[0].val;
        rest.shift();
      }
      return [text].concat(rest);
    } else {
      var text = new nodes.Text(str.substr(0, match.index));
      text.line = line;
      var buffer = [text];
      var rest = match[2];
      var range = parseJSExpression(rest);
      var inner = new Parser(range.src, this.filename, this.options);
      buffer.push(inner.parse());
      return buffer.concat(this.parseInlineTagsInText(rest.substr(range.end + 1)));
    }
  } else {
    var text = new nodes.Text(str);
    text.line = line;
    return [text];
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Parser.prototype.parseInterpolation"></a>[function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>parseInterpolation ()](#apidoc.element.jade.Parser.prototype.parseInterpolation)
- description and source-code
```javascript
parseInterpolation = function (){
  var tok = this.advance();
  var tag = new nodes.Tag(tok.val);
  tag.buffer = true;
  return this.tag(tag);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Parser.prototype.parseMixin"></a>[function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>parseMixin ()](#apidoc.element.jade.Parser.prototype.parseMixin)
- description and source-code
```javascript
parseMixin = function (){
  var tok = this.expect('mixin');
  var name = tok.val;
  var args = tok.args;
  var mixin;

  // definition
  if ('indent' == this.peek().type) {
    this.inMixin++;
    mixin = new nodes.Mixin(name, args, this.block(), false);
    this.mixins[name] = mixin;
    this.inMixin--;
    return mixin;
  // call
  } else {
    return new nodes.Mixin(name, args, null, true);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Parser.prototype.parseMixinBlock"></a>[function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>parseMixinBlock ()](#apidoc.element.jade.Parser.prototype.parseMixinBlock)
- description and source-code
```javascript
parseMixinBlock = function () {
  var block = this.expect('mixin-block');
  if (!this.inMixin) {
    throw new Error('Anonymous blocks are not allowed unless they are part of a mixin.');
  }
  return new nodes.MixinBlock();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Parser.prototype.parseTag"></a>[function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>parseTag ()](#apidoc.element.jade.Parser.prototype.parseTag)
- description and source-code
```javascript
parseTag = function (){
  var tok = this.advance();
  var tag = new nodes.Tag(tok.val);

  tag.selfClosing = tok.selfClosing;

  return this.tag(tag);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Parser.prototype.parseText"></a>[function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>parseText ()](#apidoc.element.jade.Parser.prototype.parseText)
- description and source-code
```javascript
parseText = function (){
  var tok = this.expect('text');
  var tokens = this.parseInlineTagsInText(tok.val);
  if (tokens.length === 1) return tokens[0];
  var node = new nodes.Block;
  for (var i = 0; i < tokens.length; i++) {
    node.push(tokens[i]);
  };
  return node;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Parser.prototype.parseTextBlock"></a>[function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>parseTextBlock ()](#apidoc.element.jade.Parser.prototype.parseTextBlock)
- description and source-code
```javascript
parseTextBlock = function (){
  var block = new nodes.Block;
  block.line = this.line();
  var body = this.peek();
  if (body.type !== 'pipeless-text') return;
  this.advance();
  block.nodes = body.val.reduce(function (accumulator, text) {
    return accumulator.concat(this.parseInlineTagsInText(text));
  }.bind(this), []);
  return block;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Parser.prototype.parseWhen"></a>[function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>parseWhen ()](#apidoc.element.jade.Parser.prototype.parseWhen)
- description and source-code
```javascript
parseWhen = function (){
  var val = this.expect('when').val;
  if (this.peek().type !== 'newline')
    return new nodes.Case.When(val, this.parseBlockExpansion());
  else
    return new nodes.Case.When(val);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Parser.prototype.peek"></a>[function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>peek ()](#apidoc.element.jade.Parser.prototype.peek)
- description and source-code
```javascript
peek = function () {
  return this.lookahead(1);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Parser.prototype.resolvePath"></a>[function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>resolvePath (path, purpose)](#apidoc.element.jade.Parser.prototype.resolvePath)
- description and source-code
```javascript
resolvePath = function (path, purpose) {
  var p = require('path');
  var dirname = p.dirname;
  var basename = p.basename;
  var join = p.join;

  if (path[0] !== '/' && !this.filename)
    throw new Error('the "filename" option is required to use "' + purpose + '" with "relative" paths');

  if (path[0] === '/' && !this.options.basedir)
    throw new Error('the "basedir" option is required to use "' + purpose + '" with "absolute" paths');

  path = join(path[0] === '/' ? this.options.basedir : dirname(this.filename), path);

  if (basename(path).indexOf('.') === -1) path += '.jade';

  return path;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.Parser.prototype.tag"></a>[function <span class="apidocSignatureSpan">jade.Parser.prototype.</span>tag (tag)](#apidoc.element.jade.Parser.prototype.tag)
- description and source-code
```javascript
tag = function (tag){
  tag.line = this.line();

  var seenAttrs = false;
  // (attrs | class | id)*
  out:
    while (true) {
      switch (this.peek().type) {
        case 'id':
        case 'class':
          var tok = this.advance();
          tag.setAttribute(tok.type, "'" + tok.val + "'");
          continue;
        case 'attrs':
          if (seenAttrs) {
            console.warn(this.filename + ', line ' + this.peek().line + ':\nYou should not have jade tags with multiple attributes
.');
          }
          seenAttrs = true;
          var tok = this.advance();
          var attrs = tok.attrs;

          if (tok.selfClosing) tag.selfClosing = true;

          for (var i = 0; i < attrs.length; i++) {
            tag.setAttribute(attrs[i].name, attrs[i].val, attrs[i].escaped);
          }
          continue;
        case '&attributes':
          var tok = this.advance();
          tag.addAttributes(tok.val);
          break;
        default:
          break out;
      }
    }

  // check immediate '.'
  if ('dot' == this.peek().type) {
    tag.textOnly = true;
    this.advance();
  }

  // (text | code | ':')?
  switch (this.peek().type) {
    case 'text':
      tag.block.push(this.parseText());
      break;
    case 'code':
      tag.code = this.parseCode();
      break;
    case ':':
      this.advance();
      tag.block = new nodes.Block;
      tag.block.push(this.parseExpr());
      break;
    case 'newline':
    case 'indent':
    case 'outdent':
    case 'eos':
    case 'pipeless-text':
      break;
    default:
      throw new Error('Unexpected token '' + this.peek().type + '' expected 'text', 'code', ':', 'newline' or 'eos'')
  }

  // newline*
  while ('newline' == this.peek().type) this.advance();

  // block?
  if (tag.textOnly) {
    tag.block = this.parseTextBlock() || new nodes.Block();
  } else if ('indent' == this.peek().type) {
    var block = this.block();
    for (var i = 0, len = block.nodes.length; i < len; ++i) {
      tag.block.push(block.nodes[i]);
    }
  }

  return tag;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jade.nodes"></a>[module jade.nodes](#apidoc.module.jade.nodes)

#### <a name="apidoc.element.jade.nodes.Block"></a>[function <span class="apidocSignatureSpan">jade.nodes.</span>Block (node)](#apidoc.element.jade.nodes.Block)
- description and source-code
```javascript
function Block(node){
  this.nodes = [];
  if (node) this.push(node);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.nodes.BlockComment"></a>[function <span class="apidocSignatureSpan">jade.nodes.</span>BlockComment (val, block, buffer)](#apidoc.element.jade.nodes.BlockComment)
- description and source-code
```javascript
function BlockComment(val, block, buffer) {
  this.block = block;
  this.val = val;
  this.buffer = buffer;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.nodes.Case"></a>[function <span class="apidocSignatureSpan">jade.nodes.</span>Case (expr, block)](#apidoc.element.jade.nodes.Case)
- description and source-code
```javascript
function Case(expr, block){
  this.expr = expr;
  this.block = block;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.nodes.Code"></a>[function <span class="apidocSignatureSpan">jade.nodes.</span>Code (val, buffer, escape)](#apidoc.element.jade.nodes.Code)
- description and source-code
```javascript
function Code(val, buffer, escape) {
  this.val = val;
  this.buffer = buffer;
  this.escape = escape;
  if (val.match(/^ *else/)) this.debug = false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.nodes.Comment"></a>[function <span class="apidocSignatureSpan">jade.nodes.</span>Comment (val, buffer)](#apidoc.element.jade.nodes.Comment)
- description and source-code
```javascript
function Comment(val, buffer) {
  this.val = val;
  this.buffer = buffer;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.nodes.Doctype"></a>[function <span class="apidocSignatureSpan">jade.nodes.</span>Doctype (val)](#apidoc.element.jade.nodes.Doctype)
- description and source-code
```javascript
function Doctype(val) {
  this.val = val;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.nodes.Each"></a>[function <span class="apidocSignatureSpan">jade.nodes.</span>Each (obj, val, key, block)](#apidoc.element.jade.nodes.Each)
- description and source-code
```javascript
function Each(obj, val, key, block) {
  this.obj = obj;
  this.val = val;
  this.key = key;
  this.block = block;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.nodes.Filter"></a>[function <span class="apidocSignatureSpan">jade.nodes.</span>Filter (name, block, attrs)](#apidoc.element.jade.nodes.Filter)
- description and source-code
```javascript
function Filter(name, block, attrs) {
  this.name = name;
  this.block = block;
  this.attrs = attrs;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.nodes.Literal"></a>[function <span class="apidocSignatureSpan">jade.nodes.</span>Literal (str)](#apidoc.element.jade.nodes.Literal)
- description and source-code
```javascript
function Literal(str) {
  this.str = str;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.nodes.Mixin"></a>[function <span class="apidocSignatureSpan">jade.nodes.</span>Mixin (name, args, block, call)](#apidoc.element.jade.nodes.Mixin)
- description and source-code
```javascript
function Mixin(name, args, block, call){
  Attrs.call(this);
  this.name = name;
  this.args = args;
  this.block = block;
  this.call = call;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.nodes.MixinBlock"></a>[function <span class="apidocSignatureSpan">jade.nodes.</span>MixinBlock ()](#apidoc.element.jade.nodes.MixinBlock)
- description and source-code
```javascript
function MixinBlock(){}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.nodes.Node"></a>[function <span class="apidocSignatureSpan">jade.nodes.</span>Node ()](#apidoc.element.jade.nodes.Node)
- description and source-code
```javascript
function Node(){}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.nodes.Tag"></a>[function <span class="apidocSignatureSpan">jade.nodes.</span>Tag (name, block)](#apidoc.element.jade.nodes.Tag)
- description and source-code
```javascript
function Tag(name, block) {
  Attrs.call(this);
  this.name = name;
  this.block = block || new Block;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.nodes.Text"></a>[function <span class="apidocSignatureSpan">jade.nodes.</span>Text (line)](#apidoc.element.jade.nodes.Text)
- description and source-code
```javascript
function Text(line) {
  this.val = line;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jade.nodes.Block"></a>[module jade.nodes.Block](#apidoc.module.jade.nodes.Block)

#### <a name="apidoc.element.jade.nodes.Block.Block"></a>[function <span class="apidocSignatureSpan">jade.nodes.</span>Block (node)](#apidoc.element.jade.nodes.Block.Block)
- description and source-code
```javascript
function Block(node){
  this.nodes = [];
  if (node) this.push(node);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jade.nodes.Block.prototype"></a>[module jade.nodes.Block.prototype](#apidoc.module.jade.nodes.Block.prototype)

#### <a name="apidoc.element.jade.nodes.Block.prototype.clone"></a>[function <span class="apidocSignatureSpan">jade.nodes.Block.prototype.</span>clone ()](#apidoc.element.jade.nodes.Block.prototype.clone)
- description and source-code
```javascript
clone = function (){
  var err = new Error('block.clone is deprecated and will be removed in v2.0.0');
  console.warn(err.stack);

  var clone = new Block;
  for (var i = 0, len = this.nodes.length; i < len; ++i) {
    clone.push(this.nodes[i].clone());
  }
  return clone;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.nodes.Block.prototype.constructor"></a>[function <span class="apidocSignatureSpan">jade.nodes.Block.prototype.</span>constructor (node)](#apidoc.element.jade.nodes.Block.prototype.constructor)
- description and source-code
```javascript
function Block(node){
  this.nodes = [];
  if (node) this.push(node);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.nodes.Block.prototype.includeBlock"></a>[function <span class="apidocSignatureSpan">jade.nodes.Block.prototype.</span>includeBlock ()](#apidoc.element.jade.nodes.Block.prototype.includeBlock)
- description and source-code
```javascript
includeBlock = function (){
  var ret = this
    , node;

  for (var i = 0, len = this.nodes.length; i < len; ++i) {
    node = this.nodes[i];
    if (node.yield) return node;
    else if (node.textOnly) continue;
    else if (node.includeBlock) ret = node.includeBlock();
    else if (node.block && !node.block.isEmpty()) ret = node.block.includeBlock();
    if (ret.yield) return ret;
  }

  return ret;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.nodes.Block.prototype.isEmpty"></a>[function <span class="apidocSignatureSpan">jade.nodes.Block.prototype.</span>isEmpty ()](#apidoc.element.jade.nodes.Block.prototype.isEmpty)
- description and source-code
```javascript
isEmpty = function (){
  return 0 == this.nodes.length;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.nodes.Block.prototype.push"></a>[function <span class="apidocSignatureSpan">jade.nodes.Block.prototype.</span>push (node)](#apidoc.element.jade.nodes.Block.prototype.push)
- description and source-code
```javascript
push = function (node){
  return this.nodes.push(node);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.nodes.Block.prototype.replace"></a>[function <span class="apidocSignatureSpan">jade.nodes.Block.prototype.</span>replace (other)](#apidoc.element.jade.nodes.Block.prototype.replace)
- description and source-code
```javascript
replace = function (other){
  var err = new Error('block.replace is deprecated and will be removed in v2.0.0');
  console.warn(err.stack);

  other.nodes = this.nodes;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.nodes.Block.prototype.unshift"></a>[function <span class="apidocSignatureSpan">jade.nodes.Block.prototype.</span>unshift (node)](#apidoc.element.jade.nodes.Block.prototype.unshift)
- description and source-code
```javascript
unshift = function (node){
  return this.nodes.unshift(node);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jade.nodes.BlockComment"></a>[module jade.nodes.BlockComment](#apidoc.module.jade.nodes.BlockComment)

#### <a name="apidoc.element.jade.nodes.BlockComment.BlockComment"></a>[function <span class="apidocSignatureSpan">jade.nodes.</span>BlockComment (val, block, buffer)](#apidoc.element.jade.nodes.BlockComment.BlockComment)
- description and source-code
```javascript
function BlockComment(val, block, buffer) {
  this.block = block;
  this.val = val;
  this.buffer = buffer;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jade.nodes.BlockComment.prototype"></a>[module jade.nodes.BlockComment.prototype](#apidoc.module.jade.nodes.BlockComment.prototype)

#### <a name="apidoc.element.jade.nodes.BlockComment.prototype.constructor"></a>[function <span class="apidocSignatureSpan">jade.nodes.BlockComment.prototype.</span>constructor (val, block, buffer)](#apidoc.element.jade.nodes.BlockComment.prototype.constructor)
- description and source-code
```javascript
function BlockComment(val, block, buffer) {
  this.block = block;
  this.val = val;
  this.buffer = buffer;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jade.nodes.Case"></a>[module jade.nodes.Case](#apidoc.module.jade.nodes.Case)

#### <a name="apidoc.element.jade.nodes.Case.Case"></a>[function <span class="apidocSignatureSpan">jade.nodes.</span>Case (expr, block)](#apidoc.element.jade.nodes.Case.Case)
- description and source-code
```javascript
function Case(expr, block){
  this.expr = expr;
  this.block = block;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.nodes.Case.When"></a>[function <span class="apidocSignatureSpan">jade.nodes.Case.</span>When (expr, block)](#apidoc.element.jade.nodes.Case.When)
- description and source-code
```javascript
function When(expr, block){
  this.expr = expr;
  this.block = block;
  this.debug = false;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jade.nodes.Case.When.prototype"></a>[module jade.nodes.Case.When.prototype](#apidoc.module.jade.nodes.Case.When.prototype)

#### <a name="apidoc.element.jade.nodes.Case.When.prototype.constructor"></a>[function <span class="apidocSignatureSpan">jade.nodes.Case.When.prototype.</span>constructor (expr, block)](#apidoc.element.jade.nodes.Case.When.prototype.constructor)
- description and source-code
```javascript
function When(expr, block){
  this.expr = expr;
  this.block = block;
  this.debug = false;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jade.nodes.Case.prototype"></a>[module jade.nodes.Case.prototype](#apidoc.module.jade.nodes.Case.prototype)

#### <a name="apidoc.element.jade.nodes.Case.prototype.constructor"></a>[function <span class="apidocSignatureSpan">jade.nodes.Case.prototype.</span>constructor (expr, block)](#apidoc.element.jade.nodes.Case.prototype.constructor)
- description and source-code
```javascript
function Case(expr, block){
  this.expr = expr;
  this.block = block;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jade.nodes.Code"></a>[module jade.nodes.Code](#apidoc.module.jade.nodes.Code)

#### <a name="apidoc.element.jade.nodes.Code.Code"></a>[function <span class="apidocSignatureSpan">jade.nodes.</span>Code (val, buffer, escape)](#apidoc.element.jade.nodes.Code.Code)
- description and source-code
```javascript
function Code(val, buffer, escape) {
  this.val = val;
  this.buffer = buffer;
  this.escape = escape;
  if (val.match(/^ *else/)) this.debug = false;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jade.nodes.Code.prototype"></a>[module jade.nodes.Code.prototype](#apidoc.module.jade.nodes.Code.prototype)

#### <a name="apidoc.element.jade.nodes.Code.prototype.constructor"></a>[function <span class="apidocSignatureSpan">jade.nodes.Code.prototype.</span>constructor (val, buffer, escape)](#apidoc.element.jade.nodes.Code.prototype.constructor)
- description and source-code
```javascript
function Code(val, buffer, escape) {
  this.val = val;
  this.buffer = buffer;
  this.escape = escape;
  if (val.match(/^ *else/)) this.debug = false;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jade.nodes.Comment"></a>[module jade.nodes.Comment](#apidoc.module.jade.nodes.Comment)

#### <a name="apidoc.element.jade.nodes.Comment.Comment"></a>[function <span class="apidocSignatureSpan">jade.nodes.</span>Comment (val, buffer)](#apidoc.element.jade.nodes.Comment.Comment)
- description and source-code
```javascript
function Comment(val, buffer) {
  this.val = val;
  this.buffer = buffer;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jade.nodes.Comment.prototype"></a>[module jade.nodes.Comment.prototype](#apidoc.module.jade.nodes.Comment.prototype)

#### <a name="apidoc.element.jade.nodes.Comment.prototype.constructor"></a>[function <span class="apidocSignatureSpan">jade.nodes.Comment.prototype.</span>constructor (val, buffer)](#apidoc.element.jade.nodes.Comment.prototype.constructor)
- description and source-code
```javascript
function Comment(val, buffer) {
  this.val = val;
  this.buffer = buffer;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jade.nodes.Doctype"></a>[module jade.nodes.Doctype](#apidoc.module.jade.nodes.Doctype)

#### <a name="apidoc.element.jade.nodes.Doctype.Doctype"></a>[function <span class="apidocSignatureSpan">jade.nodes.</span>Doctype (val)](#apidoc.element.jade.nodes.Doctype.Doctype)
- description and source-code
```javascript
function Doctype(val) {
  this.val = val;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jade.nodes.Doctype.prototype"></a>[module jade.nodes.Doctype.prototype](#apidoc.module.jade.nodes.Doctype.prototype)

#### <a name="apidoc.element.jade.nodes.Doctype.prototype.constructor"></a>[function <span class="apidocSignatureSpan">jade.nodes.Doctype.prototype.</span>constructor (val)](#apidoc.element.jade.nodes.Doctype.prototype.constructor)
- description and source-code
```javascript
function Doctype(val) {
  this.val = val;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jade.nodes.Each"></a>[module jade.nodes.Each](#apidoc.module.jade.nodes.Each)

#### <a name="apidoc.element.jade.nodes.Each.Each"></a>[function <span class="apidocSignatureSpan">jade.nodes.</span>Each (obj, val, key, block)](#apidoc.element.jade.nodes.Each.Each)
- description and source-code
```javascript
function Each(obj, val, key, block) {
  this.obj = obj;
  this.val = val;
  this.key = key;
  this.block = block;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jade.nodes.Each.prototype"></a>[module jade.nodes.Each.prototype](#apidoc.module.jade.nodes.Each.prototype)

#### <a name="apidoc.element.jade.nodes.Each.prototype.constructor"></a>[function <span class="apidocSignatureSpan">jade.nodes.Each.prototype.</span>constructor (obj, val, key, block)](#apidoc.element.jade.nodes.Each.prototype.constructor)
- description and source-code
```javascript
function Each(obj, val, key, block) {
  this.obj = obj;
  this.val = val;
  this.key = key;
  this.block = block;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jade.nodes.Filter"></a>[module jade.nodes.Filter](#apidoc.module.jade.nodes.Filter)

#### <a name="apidoc.element.jade.nodes.Filter.Filter"></a>[function <span class="apidocSignatureSpan">jade.nodes.</span>Filter (name, block, attrs)](#apidoc.element.jade.nodes.Filter.Filter)
- description and source-code
```javascript
function Filter(name, block, attrs) {
  this.name = name;
  this.block = block;
  this.attrs = attrs;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jade.nodes.Filter.prototype"></a>[module jade.nodes.Filter.prototype](#apidoc.module.jade.nodes.Filter.prototype)

#### <a name="apidoc.element.jade.nodes.Filter.prototype.constructor"></a>[function <span class="apidocSignatureSpan">jade.nodes.Filter.prototype.</span>constructor (name, block, attrs)](#apidoc.element.jade.nodes.Filter.prototype.constructor)
- description and source-code
```javascript
function Filter(name, block, attrs) {
  this.name = name;
  this.block = block;
  this.attrs = attrs;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jade.nodes.Literal"></a>[module jade.nodes.Literal](#apidoc.module.jade.nodes.Literal)

#### <a name="apidoc.element.jade.nodes.Literal.Literal"></a>[function <span class="apidocSignatureSpan">jade.nodes.</span>Literal (str)](#apidoc.element.jade.nodes.Literal.Literal)
- description and source-code
```javascript
function Literal(str) {
  this.str = str;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jade.nodes.Literal.prototype"></a>[module jade.nodes.Literal.prototype](#apidoc.module.jade.nodes.Literal.prototype)

#### <a name="apidoc.element.jade.nodes.Literal.prototype.constructor"></a>[function <span class="apidocSignatureSpan">jade.nodes.Literal.prototype.</span>constructor (str)](#apidoc.element.jade.nodes.Literal.prototype.constructor)
- description and source-code
```javascript
function Literal(str) {
  this.str = str;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jade.nodes.Mixin"></a>[module jade.nodes.Mixin](#apidoc.module.jade.nodes.Mixin)

#### <a name="apidoc.element.jade.nodes.Mixin.Mixin"></a>[function <span class="apidocSignatureSpan">jade.nodes.</span>Mixin (name, args, block, call)](#apidoc.element.jade.nodes.Mixin.Mixin)
- description and source-code
```javascript
function Mixin(name, args, block, call){
  Attrs.call(this);
  this.name = name;
  this.args = args;
  this.block = block;
  this.call = call;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jade.nodes.Mixin.prototype"></a>[module jade.nodes.Mixin.prototype](#apidoc.module.jade.nodes.Mixin.prototype)

#### <a name="apidoc.element.jade.nodes.Mixin.prototype.constructor"></a>[function <span class="apidocSignatureSpan">jade.nodes.Mixin.prototype.</span>constructor (name, args, block, call)](#apidoc.element.jade.nodes.Mixin.prototype.constructor)
- description and source-code
```javascript
function Mixin(name, args, block, call){
  Attrs.call(this);
  this.name = name;
  this.args = args;
  this.block = block;
  this.call = call;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jade.nodes.MixinBlock"></a>[module jade.nodes.MixinBlock](#apidoc.module.jade.nodes.MixinBlock)

#### <a name="apidoc.element.jade.nodes.MixinBlock.MixinBlock"></a>[function <span class="apidocSignatureSpan">jade.nodes.</span>MixinBlock ()](#apidoc.element.jade.nodes.MixinBlock.MixinBlock)
- description and source-code
```javascript
function MixinBlock(){}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jade.nodes.MixinBlock.prototype"></a>[module jade.nodes.MixinBlock.prototype](#apidoc.module.jade.nodes.MixinBlock.prototype)

#### <a name="apidoc.element.jade.nodes.MixinBlock.prototype.constructor"></a>[function <span class="apidocSignatureSpan">jade.nodes.MixinBlock.prototype.</span>constructor ()](#apidoc.element.jade.nodes.MixinBlock.prototype.constructor)
- description and source-code
```javascript
function MixinBlock(){}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jade.nodes.Node"></a>[module jade.nodes.Node](#apidoc.module.jade.nodes.Node)

#### <a name="apidoc.element.jade.nodes.Node.Node"></a>[function <span class="apidocSignatureSpan">jade.nodes.</span>Node ()](#apidoc.element.jade.nodes.Node.Node)
- description and source-code
```javascript
function Node(){}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jade.nodes.Node.prototype"></a>[module jade.nodes.Node.prototype](#apidoc.module.jade.nodes.Node.prototype)

#### <a name="apidoc.element.jade.nodes.Node.prototype.clone"></a>[function <span class="apidocSignatureSpan">jade.nodes.Node.prototype.</span>clone ()](#apidoc.element.jade.nodes.Node.prototype.clone)
- description and source-code
```javascript
clone = function (){
  var err = new Error('node.clone is deprecated and will be removed in v2.0.0');
  console.warn(err.stack);
  return this;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jade.nodes.Tag"></a>[module jade.nodes.Tag](#apidoc.module.jade.nodes.Tag)

#### <a name="apidoc.element.jade.nodes.Tag.Tag"></a>[function <span class="apidocSignatureSpan">jade.nodes.</span>Tag (name, block)](#apidoc.element.jade.nodes.Tag.Tag)
- description and source-code
```javascript
function Tag(name, block) {
  Attrs.call(this);
  this.name = name;
  this.block = block || new Block;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jade.nodes.Tag.prototype"></a>[module jade.nodes.Tag.prototype](#apidoc.module.jade.nodes.Tag.prototype)

#### <a name="apidoc.element.jade.nodes.Tag.prototype.canInline"></a>[function <span class="apidocSignatureSpan">jade.nodes.Tag.prototype.</span>canInline ()](#apidoc.element.jade.nodes.Tag.prototype.canInline)
- description and source-code
```javascript
canInline = function (){
  var nodes = this.block.nodes;

  function isInline(node){
    // Recurse if the node is a block
    if (node.isBlock) return node.nodes.every(isInline);
    return node.isText || (node.isInline && node.isInline());
  }

  // Empty tag
  if (!nodes.length) return true;

  // Text-only or inline-only tag
  if (1 == nodes.length) return isInline(nodes[0]);

  // Multi-line inline-only tag
  if (this.block.nodes.every(isInline)) {
    for (var i = 1, len = nodes.length; i < len; ++i) {
      if (nodes[i-1].isText && nodes[i].isText)
        return false;
    }
    return true;
  }

  // Mixed tag
  return false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.nodes.Tag.prototype.clone"></a>[function <span class="apidocSignatureSpan">jade.nodes.Tag.prototype.</span>clone ()](#apidoc.element.jade.nodes.Tag.prototype.clone)
- description and source-code
```javascript
clone = function (){
  var err = new Error('tag.clone is deprecated and will be removed in v2.0.0');
  console.warn(err.stack);

  var clone = new Tag(this.name, this.block.clone());
  clone.line = this.line;
  clone.attrs = this.attrs;
  clone.textOnly = this.textOnly;
  return clone;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.nodes.Tag.prototype.constructor"></a>[function <span class="apidocSignatureSpan">jade.nodes.Tag.prototype.</span>constructor (name, block)](#apidoc.element.jade.nodes.Tag.prototype.constructor)
- description and source-code
```javascript
function Tag(name, block) {
  Attrs.call(this);
  this.name = name;
  this.block = block || new Block;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.nodes.Tag.prototype.isInline"></a>[function <span class="apidocSignatureSpan">jade.nodes.Tag.prototype.</span>isInline ()](#apidoc.element.jade.nodes.Tag.prototype.isInline)
- description and source-code
```javascript
isInline = function (){
  return ~inlineTags.indexOf(this.name);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jade.nodes.Text"></a>[module jade.nodes.Text](#apidoc.module.jade.nodes.Text)

#### <a name="apidoc.element.jade.nodes.Text.Text"></a>[function <span class="apidocSignatureSpan">jade.nodes.</span>Text (line)](#apidoc.element.jade.nodes.Text.Text)
- description and source-code
```javascript
function Text(line) {
  this.val = line;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jade.nodes.Text.prototype"></a>[module jade.nodes.Text.prototype](#apidoc.module.jade.nodes.Text.prototype)

#### <a name="apidoc.element.jade.nodes.Text.prototype.constructor"></a>[function <span class="apidocSignatureSpan">jade.nodes.Text.prototype.</span>constructor (line)](#apidoc.element.jade.nodes.Text.prototype.constructor)
- description and source-code
```javascript
function Text(line) {
  this.val = line;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jade.runtime"></a>[module jade.runtime](#apidoc.module.jade.runtime)

#### <a name="apidoc.element.jade.runtime.DebugItem"></a>[function <span class="apidocSignatureSpan">jade.runtime.</span>DebugItem (lineno, filename)](#apidoc.element.jade.runtime.DebugItem)
- description and source-code
```javascript
function DebugItem(lineno, filename) {
  this.lineno = lineno;
  this.filename = filename;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.runtime.attr"></a>[function <span class="apidocSignatureSpan">jade.runtime.</span>attr (key, val, escaped, terse)](#apidoc.element.jade.runtime.attr)
- description and source-code
```javascript
function attr(key, val, escaped, terse) {
  if (key === 'style') {
    val = exports.style(val);
  }
  if ('boolean' == typeof val || null == val) {
    if (val) {
      return ' ' + (terse ? key : key + '="' + key + '"');
    } else {
      return '';
    }
  } else if (0 == key.indexOf('data') && 'string' != typeof val) {
    if (JSON.stringify(val).indexOf('&') !== -1) {
      console.warn('Since Jade 2.0.0, ampersands ('&') in data attributes ' +
                   'will be escaped to '&amp;'');
    };
    if (val && typeof val.toISOString === 'function') {
      console.warn('Jade will eliminate the double quotes around dates in ' +
                   'ISO form after 2.0.0');
    }
    return ' ' + key + "='" + JSON.stringify(val).replace(/'/g, '&apos;') + "'";
  } else if (escaped) {
    if (val && typeof val.toISOString === 'function') {
      console.warn('Jade will stringify dates in ISO form after 2.0.0');
    }
    return ' ' + key + '="' + exports.escape(val) + '"';
  } else {
    if (val && typeof val.toISOString === 'function') {
      console.warn('Jade will stringify dates in ISO form after 2.0.0');
    }
    return ' ' + key + '="' + val + '"';
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.runtime.attrs"></a>[function <span class="apidocSignatureSpan">jade.runtime.</span>attrs (obj, terse)](#apidoc.element.jade.runtime.attrs)
- description and source-code
```javascript
function attrs(obj, terse){
  var buf = [];

  var keys = Object.keys(obj);

  if (keys.length) {
    for (var i = 0; i < keys.length; ++i) {
      var key = keys[i]
        , val = obj[key];

      if ('class' == key) {
        if (val = joinClasses(val)) {
          buf.push(' ' + key + '="' + val + '"');
        }
      } else {
        buf.push(exports.attr(key, val, false, terse));
      }
    }
  }

  return buf.join('');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.runtime.cls"></a>[function <span class="apidocSignatureSpan">jade.runtime.</span>cls (classes, escaped)](#apidoc.element.jade.runtime.cls)
- description and source-code
```javascript
function cls(classes, escaped) {
  var buf = [];
  for (var i = 0; i < classes.length; i++) {
    if (escaped && escaped[i]) {
      buf.push(exports.escape(joinClasses([classes[i]])));
    } else {
      buf.push(joinClasses(classes[i]));
    }
  }
  var text = joinClasses(buf);
  if (text.length) {
    return ' class="' + text + '"';
  } else {
    return '';
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.runtime.escape"></a>[function <span class="apidocSignatureSpan">jade.runtime.</span>escape (html)](#apidoc.element.jade.runtime.escape)
- description and source-code
```javascript
function jade_escape(html){
  var result = String(html).replace(jade_match_html, jade_encode_char);
  if (result === '' + html) return html;
  else return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.runtime.joinClasses"></a>[function <span class="apidocSignatureSpan">jade.runtime.</span>joinClasses (val)](#apidoc.element.jade.runtime.joinClasses)
- description and source-code
```javascript
function joinClasses(val) {
  return (Array.isArray(val) ? val.map(joinClasses) :
    (val && typeof val === 'object') ? Object.keys(val).filter(function (key) { return val[key]; }) :
    [val]).filter(nulls).join(' ');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.runtime.merge"></a>[function <span class="apidocSignatureSpan">jade.runtime.</span>merge (a, b)](#apidoc.element.jade.runtime.merge)
- description and source-code
```javascript
function merge(a, b) {
  if (arguments.length === 1) {
    var attrs = a[0];
    for (var i = 1; i < a.length; i++) {
      attrs = merge(attrs, a[i]);
    }
    return attrs;
  }
  var ac = a['class'];
  var bc = b['class'];

  if (ac || bc) {
    ac = ac || [];
    bc = bc || [];
    if (!Array.isArray(ac)) ac = [ac];
    if (!Array.isArray(bc)) bc = [bc];
    a['class'] = ac.concat(bc).filter(nulls);
  }

  for (var key in b) {
    if (key != 'class') {
      a[key] = b[key];
    }
  }

  return a;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.runtime.rethrow"></a>[function <span class="apidocSignatureSpan">jade.runtime.</span>rethrow (err, filename, lineno, str)](#apidoc.element.jade.runtime.rethrow)
- description and source-code
```javascript
function rethrow(err, filename, lineno, str){
  if (!(err instanceof Error)) throw err;
  if ((typeof window != 'undefined' || !filename) && !str) {
    err.message += ' on line ' + lineno;
    throw err;
  }
  try {
    str = str || require('fs').readFileSync(filename, 'utf8')
  } catch (ex) {
    rethrow(err, null, lineno)
  }
  var context = 3
    , lines = str.split('\n')
    , start = Math.max(lineno - context, 0)
    , end = Math.min(lines.length, lineno + context);

  // Error context
  var context = lines.slice(start, end).map(function(line, i){
    var curr = i + start + 1;
    return (curr == lineno ? '  > ' : '    ')
      + curr
      + '| '
      + line;
  }).join('\n');

  // Alter exception message
  err.path = filename;
  err.message = (filename || 'Jade') + ':' + lineno
    + '\n' + context + '\n\n' + err.message;
  throw err;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.runtime.style"></a>[function <span class="apidocSignatureSpan">jade.runtime.</span>style (val)](#apidoc.element.jade.runtime.style)
- description and source-code
```javascript
style = function (val) {
  if (val && typeof val === 'object') {
    return Object.keys(val).map(function (style) {
      return style + ':' + val[style];
    }).join(';');
  } else {
    return val;
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jade.utils"></a>[module jade.utils](#apidoc.module.jade.utils)

#### <a name="apidoc.element.jade.utils.merge"></a>[function <span class="apidocSignatureSpan">jade.utils.</span>merge (a, b)](#apidoc.element.jade.utils.merge)
- description and source-code
```javascript
merge = function (a, b) {
  for (var key in b) a[key] = b[key];
  return a;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.utils.stringify"></a>[function <span class="apidocSignatureSpan">jade.utils.</span>stringify (str)](#apidoc.element.jade.utils.stringify)
- description and source-code
```javascript
stringify = function (str) {
  return JSON.stringify(str)
             .replace(/\u2028/g, '\\u2028')
             .replace(/\u2029/g, '\\u2029');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jade.utils.walkAST"></a>[function <span class="apidocSignatureSpan">jade.utils.</span>walkAST (ast, before, after)](#apidoc.element.jade.utils.walkAST)
- description and source-code
```javascript
function walkAST(ast, before, after) {
  before && before(ast);
  switch (ast.type) {
    case 'Block':
      ast.nodes.forEach(function (node) {
        walkAST(node, before, after);
      });
      break;
    case 'Case':
    case 'Each':
    case 'Mixin':
    case 'Tag':
    case 'When':
    case 'Code':
      ast.block && walkAST(ast.block, before, after);
      break;
    case 'Attrs':
    case 'BlockComment':
    case 'Comment':
    case 'Doctype':
    case 'Filter':
    case 'Literal':
    case 'MixinBlock':
    case 'Text':
      break;
    default:
      throw new Error('Unexpected node type ' + ast.type);
      break;
  }
  after && after(ast);
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
