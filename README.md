# npmtest-tldjs

#### basic test coverage for  [tldjs (v1.7.0)](https://github.com/oncletom/tld.js)  [![npm package](https://img.shields.io/npm/v/npmtest-tldjs.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-tldjs) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-tldjs.svg)](https://travis-ci.org/npmtest/node-npmtest-tldjs)

#### JavaScript API to work against complex domain names, subdomains and URIs.

[![NPM](https://nodei.co/npm/tldjs.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/tldjs)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-tldjs/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-tldjs/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-tldjs/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-tldjs/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-tldjs/build/test-report.html)|
| test-server-github : | [![github.com test-server](https://npmtest.github.io/node-npmtest-tldjs/GitHub-Mark-32px.png)](https://npmtest.github.io/node-npmtest-tldjs/build/app/index.html) | | build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-tldjs/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-tldjs/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-tldjs/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-tldjs/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-tldjs/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-tldjs/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-tldjs/build/test-report.html](https://npmtest.github.io/node-npmtest-tldjs/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-tldjs/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-tldjs/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-tldjs/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-tldjs/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-tldjs/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-tldjs/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-tldjs/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-tldjs/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Thomas Parisot",
        "url": "https://oncletom.io"
    },
    "bugs": {
        "url": "https://github.com/oncletom/tld.js/issues"
    },
    "config": {
        "blanket": {
            "pattern": "tld.js/lib/"
        },
        "travis-cov": {
            "threshold": 97
        }
    },
    "dependencies": {
        "punycode": "^1.4.1"
    },
    "description": "JavaScript API to work against complex domain names, subdomains and URIs.",
    "devDependencies": {
        "blanket": "1.1.9",
        "env-test": "^1.0.0",
        "expect.js": "^0.3.1",
        "github-changes": "^1.0.0",
        "jshint": "^2.5.1",
        "mocha": "^2.3.3",
        "phantomjs": "^1.9.18",
        "testling": "^1.7.0",
        "travis-cov": "^0.2.5"
    },
    "directories": {},
    "dist": {
        "shasum": "33de08e59d32e02f2be850096476d671b1431a81",
        "tarball": "https://registry.npmjs.org/tldjs/-/tldjs-1.7.0.tgz"
    },
    "engines": {
        "node": ">= 0.10"
    },
    "gitHead": "6b88ce2653e9c1da6dff3a6933feb06003e06e40",
    "homepage": "https://github.com/oncletom/tld.js",
    "keywords": [
        "tld",
        "sld",
        "domain",
        "browser",
        "uri",
        "url",
        "domain name",
        "subdomain",
        "public suffix"
    ],
    "license": "MIT",
    "main": "index.js",
    "maintainers": [
        {
            "name": "oncletom"
        }
    ],
    "name": "tldjs",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git://github.com/oncletom/tld.js.git"
    },
    "scripts": {
        "coverage": "npm run test-coverage -- > coverage.html",
        "generate-changelog": "github-changes -o oncletom -r 'tld.js' -n ${npm_package_version} --only-pulls --use-commit-body",
        "lint": "jshint --config .jshintrc lib/**/*.js",
        "postinstall": "node ./bin/postinstall.js",
        "posttest": "npm run lint && npm run test-browser",
        "test": "mocha -R dot -r env-test",
        "test-browser": "testling",
        "test-coverage": "mocha -R travis-cov -r blanket -r env-test",
        "test-watch": "mocha -R dot -r env-test --watch",
        "update": "node ./bin/update.js",
        "version": "npm run generate-changelog && git add CHANGELOG.md rules.json"
    },
    "testling": {
        "files": "test/*.js",
        "harness": "mocha-bdd",
        "browsers": [
            "ie/7..10",
            "ff/latest..nightly",
            "chrome/latest..canary",
            "opera/latest..next",
            "safari/6.0",
            "iphone/6.0",
            "android/4.2"
        ]
    },
    "tldjs": {
        "providers": {
            "publicsuffix-org": "https://publicsuffix.org/list/effective_tld_names.dat"
        }
    },
    "version": "1.7.0",
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
