# npmtest-fbjs

#### basic test coverage for  [fbjs (v0.8.12)](https://github.com/facebook/fbjs#readme)  [![npm package](https://img.shields.io/npm/v/npmtest-fbjs.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-fbjs) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-fbjs.svg)](https://travis-ci.org/npmtest/node-npmtest-fbjs)

#### A collection of utility libraries used by other Facebook JS projects

[![NPM](https://nodei.co/npm/fbjs.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/fbjs)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-fbjs/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-fbjs/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-fbjs/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-fbjs/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-fbjs/build/test-report.html)|
| build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-fbjs/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-fbjs/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-fbjs/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-fbjs/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-fbjs/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-fbjs/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-fbjs/build/test-report.html](https://npmtest.github.io/node-npmtest-fbjs/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-fbjs/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-fbjs/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-fbjs/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-fbjs/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-fbjs/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-fbjs/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-fbjs/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-fbjs/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "browserify": {
        "transform": [
            "loose-envify"
        ]
    },
    "bugs": {
        "url": "https://github.com/facebook/fbjs/issues"
    },
    "dependencies": {
        "core-js": "^1.0.0",
        "isomorphic-fetch": "^2.1.1",
        "loose-envify": "^1.0.0",
        "object-assign": "^4.1.0",
        "promise": "^7.1.1",
        "setimmediate": "^1.0.5",
        "ua-parser-js": "^0.7.9"
    },
    "description": "A collection of utility libraries used by other Facebook JS projects",
    "devDependencies": {
        "babel-eslint": "^6.0.3",
        "babel-preset-fbjs": "file:babel-preset",
        "del": "^2.2.0",
        "eslint": "^2.8.0",
        "fbjs-scripts": "file:scripts",
        "flow-bin": "^0.38.0",
        "gulp": "^3.9.1",
        "gulp-babel": "^6.1.2",
        "gulp-flatten": "^0.2.0",
        "gulp-rename": "^1.2.2",
        "immutable": "^3.7.6",
        "jest-cli": "^0.9.2",
        "merge-stream": "^1.0.0",
        "run-sequence": "^1.1.5"
    },
    "devEngines": {
        "node": ">=4.x",
        "npm": ">=2.x"
    },
    "directories": {},
    "dist": {
        "shasum": "10b5d92f76d45575fd63a217d4ea02bea2f8ed04",
        "tarball": "https://registry.npmjs.org/fbjs/-/fbjs-0.8.12.tgz"
    },
    "files": [
        "LICENSE",
        "PATENTS",
        "README.md",
        "flow/",
        "index.js",
        "lib/",
        "module-map.json"
    ],
    "gitHead": "a487920ee52e81b0feda06cc58fa29d04ab057f7",
    "homepage": "https://github.com/facebook/fbjs#readme",
    "jest": {
        "modulePathIgnorePatterns": [
            "/lib/",
            "/node_modules/"
        ],
        "persistModuleRegistryBetweenSpecs": true,
        "preprocessorIgnorePatterns": [
            "/node_modules/"
        ],
        "rootDir": "",
        "scriptPreprocessor": "node_modules/fbjs-scripts/jest/preprocessor.js",
        "setupEnvScriptFile": "node_modules/fbjs-scripts/jest/environment.js",
        "testPathDirs": [
            "<rootDir>/src"
        ],
        "unmockedModulePathPatterns": [
            "<rootDir>/node_modules/",
            "<rootDir>/src/(?!(__forks__/fetch.js$|fetch/))"
        ]
    },
    "license": "BSD-3-Clause",
    "main": "index.js",
    "maintainers": [
        {
            "name": "fb"
        },
        {
            "name": "josephsavona"
        },
        {
            "name": "spicyj"
        },
        {
            "name": "steveluscher"
        },
        {
            "name": "wincent"
        },
        {
            "name": "yungsters"
        },
        {
            "name": "yuzhi"
        },
        {
            "name": "zpao"
        }
    ],
    "name": "fbjs",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/facebook/fbjs.git"
    },
    "scripts": {
        "build": "gulp build",
        "lint": "eslint .",
        "postbuild": "node scripts/node/check-lib-requires.js lib",
        "prepublish": "npm run build",
        "pretest": "node node_modules/fbjs-scripts/node/check-dev-engines.js package.json",
        "test": "NODE_ENV=test jest",
        "test-babel-presets": "cd babel-preset && npm install && npm test",
        "typecheck": "flow check src"
    },
    "version": "0.8.12"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
