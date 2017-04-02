# api documentation for  [ora (v1.2.0)](https://github.com/sindresorhus/ora#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-ora.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-ora) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-ora.svg)](https://travis-ci.org/npmdoc/node-npmdoc-ora)
#### Elegant terminal spinner

[![NPM](https://nodei.co/npm/ora.png?downloads=true)](https://www.npmjs.com/package/ora)

[![apidoc](https://npmdoc.github.io/node-npmdoc-ora/build/screen-capture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-ora_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-ora/build..beta..travis-ci.org/apidoc.html)

![package-listing](https://npmdoc.github.io/node-npmdoc-ora/build/screen-capture.npmPackageListing.svg)



# package.json

```json

{
    "author": {
        "name": "Sindre Sorhus",
        "email": "sindresorhus@gmail.com",
        "url": "sindresorhus.com"
    },
    "bugs": {
        "url": "https://github.com/sindresorhus/ora/issues"
    },
    "dependencies": {
        "chalk": "^1.1.1",
        "cli-cursor": "^2.1.0",
        "cli-spinners": "^1.0.0",
        "log-symbols": "^1.0.2"
    },
    "description": "Elegant terminal spinner",
    "devDependencies": {
        "ava": "*",
        "get-stream": "^3.0.0",
        "strip-ansi": "^3.0.1",
        "xo": "*"
    },
    "directories": {},
    "dist": {
        "shasum": "32fb3183500efe83f5ea89101785f0ee6060fec9",
        "tarball": "https://registry.npmjs.org/ora/-/ora-1.2.0.tgz"
    },
    "engines": {
        "node": ">=4"
    },
    "files": [
        "index.js"
    ],
    "gitHead": "4a60987a95ecd53526a74ab62505d321a61220dd",
    "homepage": "https://github.com/sindresorhus/ora#readme",
    "keywords": [
        "cli",
        "spinner",
        "spinners",
        "terminal",
        "term",
        "console",
        "ascii",
        "unicode",
        "loading",
        "indicator",
        "progress",
        "busy",
        "wait",
        "idle"
    ],
    "license": "MIT",
    "maintainers": [
        {
            "name": "sindresorhus",
            "email": "sindresorhus@gmail.com"
        }
    ],
    "name": "ora",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/sindresorhus/ora.git"
    },
    "scripts": {
        "test": "xo && ava"
    },
    "version": "1.2.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module ora](#apidoc.module.ora)
1.  [function <span class="apidocSignatureSpan">ora.</span>promise (action, options)](#apidoc.element.ora.promise)



# <a name="apidoc.module.ora"></a>[module ora](#apidoc.module.ora)

#### <a name="apidoc.element.ora.promise"></a>[function <span class="apidocSignatureSpan">ora.</span>promise (action, options)](#apidoc.element.ora.promise)
- description and source-code
```javascript
(action, options) => {
	if (typeof action.then !== 'function') {
		throw new TypeError('Parameter 'action' must be a Promise');
	}

	const spinner = new Ora(options);
	spinner.start();

	action.then(
		() => {
			spinner.succeed();
		},
		() => {
			spinner.fail();
		}
	);

	return spinner;
}
```
- example usage
```shell
...

Change the text.

#### .color

Change the spinner color.

#### .promise(action, [options|text])

Starts a spinner for a promise. The spinner is stopped with '.succeed()' if the promise fulfills or with '.fail()' if it rejects
. Returns the spinner instance.

##### action

Type: 'Promise'
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
