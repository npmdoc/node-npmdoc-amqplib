# api documentation for  [amqplib (v0.5.1)](http://squaremo.github.io/amqp.node/)  [![npm package](https://img.shields.io/npm/v/npmdoc-amqplib.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-amqplib) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-amqplib.svg)](https://travis-ci.org/npmdoc/node-npmdoc-amqplib)
#### An AMQP 0-9-1 (e.g., RabbitMQ) library and client.

[![NPM](https://nodei.co/npm/amqplib.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/amqplib)

[![apidoc](https://npmdoc.github.io/node-npmdoc-amqplib/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-amqplib/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-amqplib/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-amqplib/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Michael Bridgen"
    },
    "bugs": {
        "url": "https://github.com/squaremo/amqp.node/issues"
    },
    "dependencies": {
        "bitsyntax": "~0.0.4",
        "bluebird": "^3.4.6",
        "buffer-more-ints": "0.0.2",
        "readable-stream": "1.x >=1.1.9"
    },
    "description": "An AMQP 0-9-1 (e.g., RabbitMQ) library and client.",
    "devDependencies": {
        "claire": "0.4.1",
        "istanbul": "0.1.x",
        "mocha": "~1",
        "uglify-js": "2.4.x"
    },
    "directories": {},
    "dist": {
        "shasum": "7cccfebabe56c2e984ea7a2243f7cefe6fbfc6cf",
        "tarball": "https://registry.npmjs.org/amqplib/-/amqplib-0.5.1.tgz"
    },
    "engines": {
        "node": ">=0.8 <6 || ^6"
    },
    "gitHead": "b21133d708fbb9677267428dd74ddb7fe7f1f80e",
    "homepage": "http://squaremo.github.io/amqp.node/",
    "keywords": [
        "AMQP",
        "AMQP 0-9-1",
        "RabbitMQ"
    ],
    "license": "MIT",
    "main": "./channel_api.js",
    "maintainers": [
        {
            "name": "squaremo"
        }
    ],
    "name": "amqplib",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/squaremo/amqp.node.git"
    },
    "scripts": {
        "prepublish": "make",
        "test": "make test"
    },
    "version": "0.5.1"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module amqplib](#apidoc.module.amqplib)
1.  [function <span class="apidocSignatureSpan">amqplib.</span>connect (url, connOptions)](#apidoc.element.amqplib.connect)
1.  object <span class="apidocSignatureSpan">amqplib.</span>credentials

#### [module amqplib.credentials](#apidoc.module.amqplib.credentials)
1.  [function <span class="apidocSignatureSpan">amqplib.credentials.</span>external ()](#apidoc.element.amqplib.credentials.external)
1.  [function <span class="apidocSignatureSpan">amqplib.credentials.</span>plain (user, passwd)](#apidoc.element.amqplib.credentials.plain)



# <a name="apidoc.module.amqplib"></a>[module amqplib](#apidoc.module.amqplib)

#### <a name="apidoc.element.amqplib.connect"></a>[function <span class="apidocSignatureSpan">amqplib.</span>connect (url, connOptions)](#apidoc.element.amqplib.connect)
- description and source-code
```javascript
function connect(url, connOptions) {
  return Promise.fromCallback(function(cb) {
    return raw_connect(url, connOptions, cb);
  })
  .then(function(conn) {
    return new ChannelModel(conn);
  });
}
```
- example usage
```shell
...
        ch.ack(msg);
      }
    });
  }
}

require('amqplib/callback_api')
  .connect('amqp://localhost', function(err, conn) {
    if (err != null) bail(err);
    consumer(conn);
    publisher(conn);
  });
'''

## Promise API example
...
```



# <a name="apidoc.module.amqplib.credentials"></a>[module amqplib.credentials](#apidoc.module.amqplib.credentials)

#### <a name="apidoc.element.amqplib.credentials.external"></a>[function <span class="apidocSignatureSpan">amqplib.credentials.</span>external ()](#apidoc.element.amqplib.credentials.external)
- description and source-code
```javascript
external = function () {
  return {
    mechanism: 'EXTERNAL',
    response: function() { return new Buffer(''); }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.amqplib.credentials.plain"></a>[function <span class="apidocSignatureSpan">amqplib.credentials.</span>plain (user, passwd)](#apidoc.element.amqplib.credentials.plain)
- description and source-code
```javascript
plain = function (user, passwd) {
  return {
    mechanism: 'PLAIN',
    response: function() {
      return new Buffer(['', user, passwd].join(String.fromCharCode(0)))
    }
  }
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
