# api documentation for  [amqplib (v0.5.1)](http://squaremo.github.io/amqp.node/)  [![npm package](https://img.shields.io/npm/v/npmdoc-amqplib.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-amqplib) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-amqplib.svg)](https://travis-ci.org/npmdoc/node-npmdoc-amqplib)
#### An AMQP 0-9-1 (e.g., RabbitMQ) library and client.

[![NPM](https://nodei.co/npm/amqplib.png?downloads=true)](https://www.npmjs.com/package/amqplib)

[![apidoc](https://npmdoc.github.io/node-npmdoc-amqplib/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-amqplib_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-amqplib/build..beta..travis-ci.org/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-amqplib/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-amqplib/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Michael Bridgen",
        "email": "mikeb@squaremobius.net"
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
            "name": "squaremo",
            "email": "mikeb@squaremobius.net"
        }
    ],
    "name": "amqplib",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
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
1.  object <span class="apidocSignatureSpan">amqplib.</span>api_args
1.  object <span class="apidocSignatureSpan">amqplib.</span>bitset
1.  object <span class="apidocSignatureSpan">amqplib.</span>callback_api
1.  object <span class="apidocSignatureSpan">amqplib.</span>callback_model
1.  object <span class="apidocSignatureSpan">amqplib.</span>channel
1.  object <span class="apidocSignatureSpan">amqplib.</span>channel_model
1.  object <span class="apidocSignatureSpan">amqplib.</span>codec
1.  object <span class="apidocSignatureSpan">amqplib.</span>connection
1.  object <span class="apidocSignatureSpan">amqplib.</span>credentials
1.  object <span class="apidocSignatureSpan">amqplib.</span>defs
1.  object <span class="apidocSignatureSpan">amqplib.</span>error
1.  object <span class="apidocSignatureSpan">amqplib.</span>format
1.  object <span class="apidocSignatureSpan">amqplib.</span>frame
1.  object <span class="apidocSignatureSpan">amqplib.</span>heartbeat
1.  object <span class="apidocSignatureSpan">amqplib.</span>mux

#### [module amqplib.api_args](#apidoc.module.amqplib.api_args)
1.  [function <span class="apidocSignatureSpan">amqplib.api_args.</span>ack (tag, allUpTo)](#apidoc.element.amqplib.api_args.ack)
1.  [function <span class="apidocSignatureSpan">amqplib.api_args.</span>assertExchange (exchange, type, options)](#apidoc.element.amqplib.api_args.assertExchange)
1.  [function <span class="apidocSignatureSpan">amqplib.api_args.</span>assertQueue (queue, options)](#apidoc.element.amqplib.api_args.assertQueue)
1.  [function <span class="apidocSignatureSpan">amqplib.api_args.</span>bindExchange (dest, source, pattern, argt)](#apidoc.element.amqplib.api_args.bindExchange)
1.  [function <span class="apidocSignatureSpan">amqplib.api_args.</span>bindQueue (queue, source, pattern, argt)](#apidoc.element.amqplib.api_args.bindQueue)
1.  [function <span class="apidocSignatureSpan">amqplib.api_args.</span>cancel (consumerTag)](#apidoc.element.amqplib.api_args.cancel)
1.  [function <span class="apidocSignatureSpan">amqplib.api_args.</span>checkExchange (exchange)](#apidoc.element.amqplib.api_args.checkExchange)
1.  [function <span class="apidocSignatureSpan">amqplib.api_args.</span>checkQueue (queue)](#apidoc.element.amqplib.api_args.checkQueue)
1.  [function <span class="apidocSignatureSpan">amqplib.api_args.</span>consume (queue, options)](#apidoc.element.amqplib.api_args.consume)
1.  [function <span class="apidocSignatureSpan">amqplib.api_args.</span>deleteExchange (exchange, options)](#apidoc.element.amqplib.api_args.deleteExchange)
1.  [function <span class="apidocSignatureSpan">amqplib.api_args.</span>deleteQueue (queue, options)](#apidoc.element.amqplib.api_args.deleteQueue)
1.  [function <span class="apidocSignatureSpan">amqplib.api_args.</span>get (queue, options)](#apidoc.element.amqplib.api_args.get)
1.  [function <span class="apidocSignatureSpan">amqplib.api_args.</span>nack (tag, allUpTo, requeue)](#apidoc.element.amqplib.api_args.nack)
1.  [function <span class="apidocSignatureSpan">amqplib.api_args.</span>prefetch (count, global)](#apidoc.element.amqplib.api_args.prefetch)
1.  [function <span class="apidocSignatureSpan">amqplib.api_args.</span>publish (exchange, routingKey, options)](#apidoc.element.amqplib.api_args.publish)
1.  [function <span class="apidocSignatureSpan">amqplib.api_args.</span>purgeQueue (queue)](#apidoc.element.amqplib.api_args.purgeQueue)
1.  [function <span class="apidocSignatureSpan">amqplib.api_args.</span>recover ()](#apidoc.element.amqplib.api_args.recover)
1.  [function <span class="apidocSignatureSpan">amqplib.api_args.</span>reject (tag, requeue)](#apidoc.element.amqplib.api_args.reject)
1.  [function <span class="apidocSignatureSpan">amqplib.api_args.</span>unbindExchange (dest, source, pattern, argt)](#apidoc.element.amqplib.api_args.unbindExchange)
1.  [function <span class="apidocSignatureSpan">amqplib.api_args.</span>unbindQueue (queue, source, pattern, argt)](#apidoc.element.amqplib.api_args.unbindQueue)

#### [module amqplib.bitset](#apidoc.module.amqplib.bitset)
1.  [function <span class="apidocSignatureSpan">amqplib.bitset.</span>BitSet (size)](#apidoc.element.amqplib.bitset.BitSet)

#### [module amqplib.callback_api](#apidoc.module.amqplib.callback_api)
1.  [function <span class="apidocSignatureSpan">amqplib.callback_api.</span>connect (url, options, cb)](#apidoc.element.amqplib.callback_api.connect)
1.  object <span class="apidocSignatureSpan">amqplib.callback_api.</span>credentials

#### [module amqplib.callback_model](#apidoc.module.amqplib.callback_model)
1.  [function <span class="apidocSignatureSpan">amqplib.callback_model.</span>CallbackModel (connection)](#apidoc.element.amqplib.callback_model.CallbackModel)
1.  [function <span class="apidocSignatureSpan">amqplib.callback_model.</span>Channel (connection)](#apidoc.element.amqplib.callback_model.Channel)
1.  [function <span class="apidocSignatureSpan">amqplib.callback_model.</span>ConfirmChannel (connection)](#apidoc.element.amqplib.callback_model.ConfirmChannel)

#### [module amqplib.channel](#apidoc.module.amqplib.channel)
1.  [function <span class="apidocSignatureSpan">amqplib.channel.</span>BaseChannel (connection)](#apidoc.element.amqplib.channel.BaseChannel)
1.  [function <span class="apidocSignatureSpan">amqplib.channel.</span>Channel (connection)](#apidoc.element.amqplib.channel.Channel)
1.  [function <span class="apidocSignatureSpan">amqplib.channel.</span>acceptMessage (continuation)](#apidoc.element.amqplib.channel.acceptMessage)

#### [module amqplib.channel_model](#apidoc.module.amqplib.channel_model)
1.  [function <span class="apidocSignatureSpan">amqplib.channel_model.</span>Channel (connection)](#apidoc.element.amqplib.channel_model.Channel)
1.  [function <span class="apidocSignatureSpan">amqplib.channel_model.</span>ChannelModel (connection)](#apidoc.element.amqplib.channel_model.ChannelModel)
1.  [function <span class="apidocSignatureSpan">amqplib.channel_model.</span>ConfirmChannel (connection)](#apidoc.element.amqplib.channel_model.ConfirmChannel)

#### [module amqplib.codec](#apidoc.module.amqplib.codec)
1.  [function <span class="apidocSignatureSpan">amqplib.codec.</span>decodeFields (slice)](#apidoc.element.amqplib.codec.decodeFields)
1.  [function <span class="apidocSignatureSpan">amqplib.codec.</span>encodeTable (buffer, val, offset)](#apidoc.element.amqplib.codec.encodeTable)

#### [module amqplib.connect](#apidoc.module.amqplib.connect)
1.  [function <span class="apidocSignatureSpan">amqplib.</span>connect (url, socketOptions, openCallback)](#apidoc.element.amqplib.connect.connect)

#### [module amqplib.connection](#apidoc.module.amqplib.connection)
1.  [function <span class="apidocSignatureSpan">amqplib.connection.</span>Connection (underlying)](#apidoc.element.amqplib.connection.Connection)
1.  [function <span class="apidocSignatureSpan">amqplib.connection.</span>isFatalError (error)](#apidoc.element.amqplib.connection.isFatalError)

#### [module amqplib.credentials](#apidoc.module.amqplib.credentials)
1.  [function <span class="apidocSignatureSpan">amqplib.credentials.</span>external ()](#apidoc.element.amqplib.credentials.external)
1.  [function <span class="apidocSignatureSpan">amqplib.credentials.</span>plain (user, passwd)](#apidoc.element.amqplib.credentials.plain)

#### [module amqplib.defs](#apidoc.module.amqplib.defs)
1.  [function <span class="apidocSignatureSpan">amqplib.defs.</span>decode (id, buf)](#apidoc.element.amqplib.defs.decode)
1.  [function <span class="apidocSignatureSpan">amqplib.defs.</span>encodeMethod (id, channel, fields)](#apidoc.element.amqplib.defs.encodeMethod)
1.  [function <span class="apidocSignatureSpan">amqplib.defs.</span>encodeProperties (id, channel, size, fields)](#apidoc.element.amqplib.defs.encodeProperties)
1.  [function <span class="apidocSignatureSpan">amqplib.defs.</span>info (id)](#apidoc.element.amqplib.defs.info)
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>AccessRequest
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>AccessRequestOk
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>BasicAck
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>BasicCancel
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>BasicCancelOk
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>BasicConsume
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>BasicConsumeOk
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>BasicDeliver
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>BasicGet
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>BasicGetEmpty
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>BasicGetOk
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>BasicNack
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>BasicProperties
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>BasicPublish
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>BasicQos
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>BasicQosOk
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>BasicRecover
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>BasicRecoverAsync
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>BasicRecoverOk
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>BasicReject
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>BasicReturn
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>ChannelClose
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>ChannelCloseOk
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>ChannelFlow
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>ChannelFlowOk
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>ChannelOpen
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>ChannelOpenOk
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>ConfirmSelect
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>ConfirmSelectOk
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>ConnectionBlocked
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>ConnectionClose
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>ConnectionCloseOk
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>ConnectionOpen
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>ConnectionOpenOk
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>ConnectionSecure
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>ConnectionSecureOk
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>ConnectionStart
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>ConnectionStartOk
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>ConnectionTune
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>ConnectionTuneOk
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>ConnectionUnblocked
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>ExchangeBind
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>ExchangeBindOk
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>ExchangeDeclare
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>ExchangeDeclareOk
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>ExchangeDelete
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>ExchangeDeleteOk
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>ExchangeUnbind
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>ExchangeUnbindOk
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>FRAME_OVERHEAD
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>QueueBind
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>QueueBindOk
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>QueueDeclare
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>QueueDeclareOk
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>QueueDelete
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>QueueDeleteOk
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>QueuePurge
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>QueuePurgeOk
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>QueueUnbind
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>QueueUnbindOk
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>TxCommit
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>TxCommitOk
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>TxRollback
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>TxRollbackOk
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>TxSelect
1.  number <span class="apidocSignatureSpan">amqplib.defs.</span>TxSelectOk
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>constant_strs
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>constants
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoAccessRequest
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoAccessRequestOk
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoBasicAck
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoBasicCancel
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoBasicCancelOk
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoBasicConsume
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoBasicConsumeOk
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoBasicDeliver
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoBasicGet
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoBasicGetEmpty
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoBasicGetOk
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoBasicNack
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoBasicPublish
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoBasicQos
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoBasicQosOk
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoBasicRecover
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoBasicRecoverAsync
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoBasicRecoverOk
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoBasicReject
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoBasicReturn
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoChannelClose
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoChannelCloseOk
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoChannelFlow
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoChannelFlowOk
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoChannelOpen
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoChannelOpenOk
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoConfirmSelect
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoConfirmSelectOk
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoConnectionBlocked
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoConnectionClose
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoConnectionCloseOk
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoConnectionOpen
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoConnectionOpenOk
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoConnectionSecure
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoConnectionSecureOk
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoConnectionStart
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoConnectionStartOk
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoConnectionTune
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoConnectionTuneOk
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoConnectionUnblocked
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoExchangeBind
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoExchangeBindOk
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoExchangeDeclare
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoExchangeDeclareOk
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoExchangeDelete
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoExchangeDeleteOk
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoExchangeUnbind
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoExchangeUnbindOk
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoQueueBind
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoQueueBindOk
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoQueueDeclare
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoQueueDeclareOk
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoQueueDelete
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoQueueDeleteOk
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoQueuePurge
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoQueuePurgeOk
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoQueueUnbind
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoQueueUnbindOk
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoTxCommit
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoTxCommitOk
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoTxRollback
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoTxRollbackOk
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoTxSelect
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>methodInfoTxSelectOk
1.  object <span class="apidocSignatureSpan">amqplib.defs.</span>propertiesInfoBasicProperties

#### [module amqplib.error](#apidoc.module.amqplib.error)
1.  [function <span class="apidocSignatureSpan">amqplib.error.</span>IllegalOperationError (msg, stack)](#apidoc.element.amqplib.error.IllegalOperationError)
1.  [function <span class="apidocSignatureSpan">amqplib.error.</span>stackCapture (reason)](#apidoc.element.amqplib.error.stackCapture)

#### [module amqplib.format](#apidoc.module.amqplib.format)
1.  [function <span class="apidocSignatureSpan">amqplib.format.</span>closeMessage (close)](#apidoc.element.amqplib.format.closeMessage)
1.  [function <span class="apidocSignatureSpan">amqplib.format.</span>inspect (frame, showFields)](#apidoc.element.amqplib.format.inspect)
1.  [function <span class="apidocSignatureSpan">amqplib.format.</span>methodName (id)](#apidoc.element.amqplib.format.methodName)

#### [module amqplib.frame](#apidoc.module.amqplib.frame)
1.  [function <span class="apidocSignatureSpan">amqplib.frame.</span>decodeFrame (frame)](#apidoc.element.amqplib.frame.decodeFrame)
1.  [function <span class="apidocSignatureSpan">amqplib.frame.</span>makeBodyFrame (channel, payload)](#apidoc.element.amqplib.frame.makeBodyFrame)
1.  [function <span class="apidocSignatureSpan">amqplib.frame.</span>parseFrame (bin, max)](#apidoc.element.amqplib.frame.parseFrame)
1.  object <span class="apidocSignatureSpan">amqplib.frame.</span>HEARTBEAT
1.  object <span class="apidocSignatureSpan">amqplib.frame.</span>HEARTBEAT_BUF
1.  string <span class="apidocSignatureSpan">amqplib.frame.</span>PROTOCOL_HEADER

#### [module amqplib.heartbeat](#apidoc.module.amqplib.heartbeat)
1.  [function <span class="apidocSignatureSpan">amqplib.heartbeat.</span>Heart (interval, checkSend, checkRecv)](#apidoc.element.amqplib.heartbeat.Heart)
1.  number <span class="apidocSignatureSpan">amqplib.heartbeat.</span>UNITS_TO_MS

#### [module amqplib.mux](#apidoc.module.amqplib.mux)
1.  [function <span class="apidocSignatureSpan">amqplib.mux.</span>Mux (downstream)](#apidoc.element.amqplib.mux.Mux)



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



# <a name="apidoc.module.amqplib.api_args"></a>[module amqplib.api_args](#apidoc.module.amqplib.api_args)

#### <a name="apidoc.element.amqplib.api_args.ack"></a>[function <span class="apidocSignatureSpan">amqplib.api_args.</span>ack (tag, allUpTo)](#apidoc.element.amqplib.api_args.ack)
- description and source-code
```javascript
ack = function (tag, allUpTo) {
  return {
    deliveryTag: tag,
    multiple: !!allUpTo
  };
}
```
- example usage
```shell
...
var ok = conn.createChannel(on_open);
function on_open(err, ch) {
  if (err != null) bail(err);
  ch.assertQueue(q);
  ch.consume(q, function(msg) {
    if (msg !== null) {
      console.log(msg.content.toString());
      ch.ack(msg);
    }
  });
}
}

require('amqplib/callback_api')
.connect('amqp://localhost', function(err, conn) {
...
```

#### <a name="apidoc.element.amqplib.api_args.assertExchange"></a>[function <span class="apidocSignatureSpan">amqplib.api_args.</span>assertExchange (exchange, type, options)](#apidoc.element.amqplib.api_args.assertExchange)
- description and source-code
```javascript
assertExchange = function (exchange, type, options) {
  options = options || EMPTY_OPTIONS;
  var argt = Object.create(options.arguments || null);
  setIfDefined(argt, 'alternate-exchange', options.alternateExchange);
  return {
    exchange: exchange,
    ticket: 0,
    type: type,
    passive: false,
    durable: (options.durable === undefined) ? true : options.durable,
    autoDelete: !!options.autoDelete,
    internal: !!options.internal,
    nowait: false,
    arguments: argt
  };
}
```
- example usage
```shell
...
                  Args.unbindQueue(queue, source, pattern, argt),
                  defs.QueueUnbindOk, cb);
};

Channel.prototype.assertExchange = function(ex, type, options, cb0) {
var cb = callbackWrapper(this, cb0);
this._rpc(defs.ExchangeDeclare,
          Args.assertExchange(ex, type, options),
          defs.ExchangeDeclareOk,
          function(e, _) { cb(e, {exchange: ex}); });
return this;
};

Channel.prototype.checkExchange = function(exchange, cb) {
return this.rpc(defs.ExchangeDeclare,
...
```

#### <a name="apidoc.element.amqplib.api_args.assertQueue"></a>[function <span class="apidocSignatureSpan">amqplib.api_args.</span>assertQueue (queue, options)](#apidoc.element.amqplib.api_args.assertQueue)
- description and source-code
```javascript
assertQueue = function (queue, options) {
  queue = queue || '';
  options = options || EMPTY_OPTIONS;

  var argt = Object.create(options.arguments || null);
  setIfDefined(argt, 'x-expires', options.expires);
  setIfDefined(argt, 'x-message-ttl', options.messageTtl);
  setIfDefined(argt, 'x-dead-letter-exchange',
               options.deadLetterExchange);
  setIfDefined(argt, 'x-dead-letter-routing-key',
               options.deadLetterRoutingKey);
  setIfDefined(argt, 'x-max-length', options.maxLength);
  setIfDefined(argt, 'x-max-priority', options.maxPriority);

  return {
    queue: queue,
    exclusive: !!options.exclusive,
    durable: (options.durable === undefined) ? true : options.durable,
    autoDelete: !!options.autoDelete,
    arguments: argt,
    passive: false,
    // deprecated but we have to include it
    ticket: 0,
    nowait: false
  };
}
```
- example usage
```shell
...
}

// Publisher
function publisher(conn) {
conn.createChannel(on_open);
function on_open(err, ch) {
  if (err != null) bail(err);
  ch.assertQueue(q);
  ch.sendToQueue(q, new Buffer('something to do'));
}
}

// Consumer
function consumer(conn) {
var ok = conn.createChannel(on_open);
...
```

#### <a name="apidoc.element.amqplib.api_args.bindExchange"></a>[function <span class="apidocSignatureSpan">amqplib.api_args.</span>bindExchange (dest, source, pattern, argt)](#apidoc.element.amqplib.api_args.bindExchange)
- description and source-code
```javascript
bindExchange = function (dest, source, pattern, argt) {
  return {
    source: source,
    destination: dest,
    routingKey: pattern,
    arguments: argt,
    ticket: 0, nowait: false
  };
}
```
- example usage
```shell
...
                Args.deleteExchange(exchange, options),
                defs.ExchangeDeleteOk, cb);
};

Channel.prototype.bindExchange =
function(dest, source, pattern, argt, cb) {
  return this.rpc(defs.ExchangeBind,
                  Args.bindExchange(dest, source, pattern, argt),
                  defs.ExchangeBindOk, cb);
};

Channel.prototype.unbindExchange =
function(dest, source, pattern, argt, cb) {
  return this.rpc(defs.ExchangeUnbind,
                  Args.unbindExchange(dest, source, pattern, argt),
...
```

#### <a name="apidoc.element.amqplib.api_args.bindQueue"></a>[function <span class="apidocSignatureSpan">amqplib.api_args.</span>bindQueue (queue, source, pattern, argt)](#apidoc.element.amqplib.api_args.bindQueue)
- description and source-code
```javascript
bindQueue = function (queue, source, pattern, argt) {
  return {
    queue: queue,
    exchange: source,
    routingKey: pattern,
    arguments: argt,
    ticket: 0, nowait: false
  };
}
```
- example usage
```shell
...
                Args.purgeQueue(queue),
                defs.QueuePurgeOk, cb);
};

Channel.prototype.bindQueue =
function(queue, source, pattern, argt, cb) {
  return this.rpc(defs.QueueBind,
                  Args.bindQueue(queue, source, pattern, argt),
                  defs.QueueBindOk, cb);
};

Channel.prototype.unbindQueue =
function(queue, source, pattern, argt, cb) {
  return this.rpc(defs.QueueUnbind,
                  Args.unbindQueue(queue, source, pattern, argt),
...
```

#### <a name="apidoc.element.amqplib.api_args.cancel"></a>[function <span class="apidocSignatureSpan">amqplib.api_args.</span>cancel (consumerTag)](#apidoc.element.amqplib.api_args.cancel)
- description and source-code
```javascript
cancel = function (consumerTag) {
  return {
    consumerTag: consumerTag,
    nowait: false
  };
}
```
- example usage
```shell
...
return this;
};

Channel.prototype.cancel = function(consumerTag, cb0) {
var cb = callbackWrapper(this, cb0);
var self = this;
this._rpc(
  defs.BasicCancel, Args.cancel(consumerTag), defs.BasicCancelOk,
  function(err, ok) {
    if (err === null) {
      self.unregisterConsumer(consumerTag);
      cb(null, ok.fields);
    }
    else cb(err);
  });
...
```

#### <a name="apidoc.element.amqplib.api_args.checkExchange"></a>[function <span class="apidocSignatureSpan">amqplib.api_args.</span>checkExchange (exchange)](#apidoc.element.amqplib.api_args.checkExchange)
- description and source-code
```javascript
checkExchange = function (exchange) {
  return {
    exchange: exchange,
    passive: true, // switch to 'may as well be another method' mode
    nowait: false,
    // ff are ignored
    durable: true, internal: false,  type: '',  autoDelete: false,
    ticket: 0
  };
}
```
- example usage
```shell
...
          defs.ExchangeDeclareOk,
          function(e, _) { cb(e, {exchange: ex}); });
return this;
};

Channel.prototype.checkExchange = function(exchange, cb) {
return this.rpc(defs.ExchangeDeclare,
                Args.checkExchange(exchange),
                defs.ExchangeDeclareOk, cb);
};

Channel.prototype.deleteExchange = function(exchange, options, cb) {
return this.rpc(defs.ExchangeDelete,
                Args.deleteExchange(exchange, options),
                defs.ExchangeDeleteOk, cb);
...
```

#### <a name="apidoc.element.amqplib.api_args.checkQueue"></a>[function <span class="apidocSignatureSpan">amqplib.api_args.</span>checkQueue (queue)](#apidoc.element.amqplib.api_args.checkQueue)
- description and source-code
```javascript
checkQueue = function (queue) {
  return {
    queue: queue,
    passive: true, // switch to "completely different" mode
    nowait: false,
    durable: true, autoDelete: false, exclusive: false, // ignored
    ticket: 0,
  };
}
```
- example usage
```shell
...
return this.rpc(defs.QueueDeclare,
                Args.assertQueue(queue, options),
                defs.QueueDeclareOk, cb);
};

Channel.prototype.checkQueue = function(queue, cb) {
return this.rpc(defs.QueueDeclare,
                Args.checkQueue(queue),
                defs.QueueDeclareOk, cb);
};

Channel.prototype.deleteQueue = function(queue, options, cb) {
return this.rpc(defs.QueueDelete,
                Args.deleteQueue(queue, options),
                defs.QueueDeleteOk, cb);
...
```

#### <a name="apidoc.element.amqplib.api_args.consume"></a>[function <span class="apidocSignatureSpan">amqplib.api_args.</span>consume (queue, options)](#apidoc.element.amqplib.api_args.consume)
- description and source-code
```javascript
consume = function (queue, options) {
  options = options || EMPTY_OPTIONS;
  var argt = Object.create(options.arguments || null);
  setIfDefined(argt, 'x-priority', options.priority);
  return {
    ticket: 0,
    queue: queue,
    consumerTag: options.consumerTag || '',
    noLocal: !!options.noLocal,
    noAck: !!options.noAck,
    exclusive: !!options.exclusive,
    nowait: false,
    arguments: argt
  };
}
```
- example usage
```shell
...

// Consumer
function consumer(conn) {
  var ok = conn.createChannel(on_open);
  function on_open(err, ch) {
    if (err != null) bail(err);
    ch.assertQueue(q);
    ch.consume(q, function(msg) {
      if (msg !== null) {
        console.log(msg.content.toString());
        ch.ack(msg);
      }
    });
  }
}
...
```

#### <a name="apidoc.element.amqplib.api_args.deleteExchange"></a>[function <span class="apidocSignatureSpan">amqplib.api_args.</span>deleteExchange (exchange, options)](#apidoc.element.amqplib.api_args.deleteExchange)
- description and source-code
```javascript
deleteExchange = function (exchange, options) {
  options = options || EMPTY_OPTIONS;
  return {
    exchange: exchange,
    ifUnused: !!options.ifUnused,
    ticket: 0, nowait: false
  };
}
```
- example usage
```shell
...
return this.rpc(defs.ExchangeDeclare,
                Args.checkExchange(exchange),
                defs.ExchangeDeclareOk, cb);
};

Channel.prototype.deleteExchange = function(exchange, options, cb) {
return this.rpc(defs.ExchangeDelete,
                Args.deleteExchange(exchange, options),
                defs.ExchangeDeleteOk, cb);
};

Channel.prototype.bindExchange =
function(dest, source, pattern, argt, cb) {
  return this.rpc(defs.ExchangeBind,
                  Args.bindExchange(dest, source, pattern, argt),
...
```

#### <a name="apidoc.element.amqplib.api_args.deleteQueue"></a>[function <span class="apidocSignatureSpan">amqplib.api_args.</span>deleteQueue (queue, options)](#apidoc.element.amqplib.api_args.deleteQueue)
- description and source-code
```javascript
deleteQueue = function (queue, options) {
  options = options || EMPTY_OPTIONS;
  return {
    queue: queue,
    ifUnused: !!options.ifUnused,
    ifEmpty: !!options.ifEmpty,
    ticket: 0, nowait: false
  };
}
```
- example usage
```shell
...
return this.rpc(defs.QueueDeclare,
                Args.checkQueue(queue),
                defs.QueueDeclareOk, cb);
};

Channel.prototype.deleteQueue = function(queue, options, cb) {
return this.rpc(defs.QueueDelete,
                Args.deleteQueue(queue, options),
                defs.QueueDeleteOk, cb);
};

Channel.prototype.purgeQueue = function(queue, cb) {
return this.rpc(defs.QueuePurge,
                Args.purgeQueue(queue),
                defs.QueuePurgeOk, cb);
...
```

#### <a name="apidoc.element.amqplib.api_args.get"></a>[function <span class="apidocSignatureSpan">amqplib.api_args.</span>get (queue, options)](#apidoc.element.amqplib.api_args.get)
- description and source-code
```javascript
get = function (queue, options) {
  options = options || EMPTY_OPTIONS;
  return {
    ticket: 0,
    queue: queue,
    noAck: !!options.noAck
  };
}
```
- example usage
```shell
...
    else cb(err);
  });
return this;
};

Channel.prototype.get = function(queue, options, cb0) {
var self = this;
var fields = Args.get(queue, options);
var cb = callbackWrapper(this, cb0);
this.sendOrEnqueue(defs.BasicGet, fields, function(err, f) {
  if (err === null) {
    if (f.id === defs.BasicGetEmpty) {
      cb(null, false);
    }
    else if (f.id === defs.BasicGetOk) {
...
```

#### <a name="apidoc.element.amqplib.api_args.nack"></a>[function <span class="apidocSignatureSpan">amqplib.api_args.</span>nack (tag, allUpTo, requeue)](#apidoc.element.amqplib.api_args.nack)
- description and source-code
```javascript
nack = function (tag, allUpTo, requeue) {
  return {
    deliveryTag: tag,
    multiple: !!allUpTo,
    requeue: (requeue === undefined) ? true : requeue
  };
}
```
- example usage
```shell
...
this.sendImmediately(defs.BasicAck, Args.ack(0, true));
return this;
};

Channel.prototype.nack = function(message, allUpTo, requeue) {
this.sendImmediately(
  defs.BasicNack,
  Args.nack(message.fields.deliveryTag, allUpTo, requeue));
return this;
};

Channel.prototype.nackAll = function(requeue) {
this.sendImmediately(
  defs.BasicNack, Args.nack(0, true, requeue))
return this;
...
```

#### <a name="apidoc.element.amqplib.api_args.prefetch"></a>[function <span class="apidocSignatureSpan">amqplib.api_args.</span>prefetch (count, global)](#apidoc.element.amqplib.api_args.prefetch)
- description and source-code
```javascript
prefetch = function (count, global) {
  return {
    prefetchCount: count || 0,
    prefetchSize: 0,
    global: !!global
  };
}
```
- example usage
```shell
...
  defs.BasicReject,
  Args.reject(message.fields.deliveryTag, requeue));
return this;
};

Channel.prototype.prefetch = function(count, global, cb) {
return this.rpc(defs.BasicQos,
                Args.prefetch(count, global),
                defs.BasicQosOk, cb);
};

Channel.prototype.recover = function(cb) {
return this.rpc(defs.BasicRecover,
                Args.recover(),
                defs.BasicRecoverOk, cb);
...
```

#### <a name="apidoc.element.amqplib.api_args.publish"></a>[function <span class="apidocSignatureSpan">amqplib.api_args.</span>publish (exchange, routingKey, options)](#apidoc.element.amqplib.api_args.publish)
- description and source-code
```javascript
publish = function (exchange, routingKey, options) {
  options = options || EMPTY_OPTIONS;

  // The CC and BCC fields expect an array of "longstr", which would
  // normally be buffer values in JavaScript; however, since a field
  // array (or table) cannot have shortstr values, the codec will
  // encode all strings as longstrs anyway.
  function convertCC(cc) {
    if (cc === undefined) {
      return undefined;
    }
    else if (Array.isArray(cc)) {
      return cc.map(String);
    }
    else return [String(cc)];
  }

  var headers = Object.create(options.headers || null);
  setIfDefined(headers, 'CC', convertCC(options.CC));
  setIfDefined(headers, 'BCC', convertCC(options.BCC));

  var deliveryMode; // undefined will default to 1 (non-persistent)

  // Previously I overloaded deliveryMode be a boolean meaning
  // 'persistent or not'; better is to name this option for what it
  // is, but I need to have backwards compatibility for applications
  // that either supply a numeric or boolean value.
  if (options.persistent !== undefined)
    deliveryMode = (options.persistent) ? 2 : 1;
  else if (typeof options.deliveryMode === 'number')
    deliveryMode = options.deliveryMode;
  else if (options.deliveryMode) // is supplied and truthy
    deliveryMode = 2;

  var expiration = options.expiration;
  if (expiration !== undefined) expiration = expiration.toString();

  return {
    // method fields
    exchange: exchange,
    routingKey: routingKey,
    mandatory: !!options.mandatory,
    immediate: false, // RabbitMQ doesn't implement this any more
    ticket: undefined,
    // properties
    contentType: options.contentType,
    contentEncoding: options.contentEncoding,
    headers: headers,
    deliveryMode: deliveryMode,
    priority: options.priority,
    correlationId: options.correlationId,
    replyTo: options.replyTo,
    expiration: expiration,
    messageId: options.messageId,
    timestamp: options.timestamp,
    type: options.type,
    userId: options.userId,
    appId: options.appId,
    clusterId: undefined
  };
}
```
- example usage
```shell
...
    return this.rpc(defs.ExchangeUnbind,
                    Args.unbindExchange(dest, source, pattern, argt),
                    defs.ExchangeUnbindOk, cb);
  };

Channel.prototype.publish =
  function(exchange, routingKey, content, options) {
    var fieldsAndProps = Args.publish(exchange, routingKey, options);
    return this.sendMessage(fieldsAndProps, fieldsAndProps, content);
  };

Channel.prototype.sendToQueue = function(queue, content, options) {
  return this.publish('', queue, content, options);
};
...
```

#### <a name="apidoc.element.amqplib.api_args.purgeQueue"></a>[function <span class="apidocSignatureSpan">amqplib.api_args.</span>purgeQueue (queue)](#apidoc.element.amqplib.api_args.purgeQueue)
- description and source-code
```javascript
purgeQueue = function (queue) {
  return {
    queue: queue,
    ticket: 0, nowait: false
  };
}
```
- example usage
```shell
...
return this.rpc(defs.QueueDelete,
                Args.deleteQueue(queue, options),
                defs.QueueDeleteOk, cb);
};

Channel.prototype.purgeQueue = function(queue, cb) {
return this.rpc(defs.QueuePurge,
                Args.purgeQueue(queue),
                defs.QueuePurgeOk, cb);
};

Channel.prototype.bindQueue =
function(queue, source, pattern, argt, cb) {
  return this.rpc(defs.QueueBind,
                  Args.bindQueue(queue, source, pattern, argt),
...
```

#### <a name="apidoc.element.amqplib.api_args.recover"></a>[function <span class="apidocSignatureSpan">amqplib.api_args.</span>recover ()](#apidoc.element.amqplib.api_args.recover)
- description and source-code
```javascript
recover = function () {
  return {requeue: true};
}
```
- example usage
```shell
...
  return this.rpc(defs.BasicQos,
                  Args.prefetch(count, global),
                  defs.BasicQosOk, cb);
};

Channel.prototype.recover = function(cb) {
  return this.rpc(defs.BasicRecover,
                  Args.recover(),
                  defs.BasicRecoverOk, cb);
};

function ConfirmChannel(connection) {
  Channel.call(this, connection);
}
inherits(ConfirmChannel, Channel);
...
```

#### <a name="apidoc.element.amqplib.api_args.reject"></a>[function <span class="apidocSignatureSpan">amqplib.api_args.</span>reject (tag, requeue)](#apidoc.element.amqplib.api_args.reject)
- description and source-code
```javascript
reject = function (tag, requeue) {
  return {
    deliveryTag: tag,
    requeue: (requeue === undefined) ? true : requeue
  };
}
```
- example usage
```shell
...
  defs.BasicNack, Args.nack(0, true, requeue))
return this;
};

Channel.prototype.reject = function(message, requeue) {
this.sendImmediately(
  defs.BasicReject,
  Args.reject(message.fields.deliveryTag, requeue));
return this;
};

Channel.prototype.prefetch = function(count, global, cb) {
return this.rpc(defs.BasicQos,
                Args.prefetch(count, global),
                defs.BasicQosOk, cb);
...
```

#### <a name="apidoc.element.amqplib.api_args.unbindExchange"></a>[function <span class="apidocSignatureSpan">amqplib.api_args.</span>unbindExchange (dest, source, pattern, argt)](#apidoc.element.amqplib.api_args.unbindExchange)
- description and source-code
```javascript
unbindExchange = function (dest, source, pattern, argt) {
  return {
    source: source,
    destination: dest,
    routingKey: pattern,
    arguments: argt,
    ticket: 0, nowait: false
  };
}
```
- example usage
```shell
...
                  Args.bindExchange(dest, source, pattern, argt),
                  defs.ExchangeBindOk, cb);
};

Channel.prototype.unbindExchange =
function(dest, source, pattern, argt, cb) {
  return this.rpc(defs.ExchangeUnbind,
                  Args.unbindExchange(dest, source, pattern, argt),
                  defs.ExchangeUnbindOk, cb);
};

Channel.prototype.publish =
function(exchange, routingKey, content, options) {
  var fieldsAndProps = Args.publish(exchange, routingKey, options);
  return this.sendMessage(fieldsAndProps, fieldsAndProps, content);
...
```

#### <a name="apidoc.element.amqplib.api_args.unbindQueue"></a>[function <span class="apidocSignatureSpan">amqplib.api_args.</span>unbindQueue (queue, source, pattern, argt)](#apidoc.element.amqplib.api_args.unbindQueue)
- description and source-code
```javascript
unbindQueue = function (queue, source, pattern, argt) {
  return {
    queue: queue,
    exchange: source,
    routingKey: pattern,
    arguments: argt,
    ticket: 0, nowait: false
  };
}
```
- example usage
```shell
...
                  Args.bindQueue(queue, source, pattern, argt),
                  defs.QueueBindOk, cb);
};

Channel.prototype.unbindQueue =
function(queue, source, pattern, argt, cb) {
  return this.rpc(defs.QueueUnbind,
                  Args.unbindQueue(queue, source, pattern, argt),
                  defs.QueueUnbindOk, cb);
};

Channel.prototype.assertExchange = function(ex, type, options, cb0) {
var cb = callbackWrapper(this, cb0);
this._rpc(defs.ExchangeDeclare,
          Args.assertExchange(ex, type, options),
...
```



# <a name="apidoc.module.amqplib.bitset"></a>[module amqplib.bitset](#apidoc.module.amqplib.bitset)

#### <a name="apidoc.element.amqplib.bitset.BitSet"></a>[function <span class="apidocSignatureSpan">amqplib.bitset.</span>BitSet (size)](#apidoc.element.amqplib.bitset.BitSet)
- description and source-code
```javascript
function BitSet(size) {
  if (size) {
    var numWords = Math.ceil(size / 32);
    this.words = new Array(numWords);
  }
  else {
    this.words = [];
  }
  this.wordsInUse = 0; // = number, not index
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.amqplib.callback_api"></a>[module amqplib.callback_api](#apidoc.module.amqplib.callback_api)

#### <a name="apidoc.element.amqplib.callback_api.connect"></a>[function <span class="apidocSignatureSpan">amqplib.callback_api.</span>connect (url, options, cb)](#apidoc.element.amqplib.callback_api.connect)
- description and source-code
```javascript
function connect(url, options, cb) {
  if (typeof url === 'function')
    cb = url, url = false, options = false;
  else if (typeof options === 'function')
    cb = options, options = false;

  raw_connect(url, options, function(err, c) {
    if (err === null) cb(null, new CallbackModel(c));
    else cb(err);
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



# <a name="apidoc.module.amqplib.callback_model"></a>[module amqplib.callback_model](#apidoc.module.amqplib.callback_model)

#### <a name="apidoc.element.amqplib.callback_model.CallbackModel"></a>[function <span class="apidocSignatureSpan">amqplib.callback_model.</span>CallbackModel (connection)](#apidoc.element.amqplib.callback_model.CallbackModel)
- description and source-code
```javascript
function CallbackModel(connection) {
  if (!(this instanceof CallbackModel))
    return new CallbackModel(connection);
  EventEmitter.call( this );
  this.connection = connection;
  var self = this;
  ['error', 'close', 'blocked', 'unblocked'].forEach(function(ev) {
    connection.on(ev, self.emit.bind(self, ev));
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.amqplib.callback_model.Channel"></a>[function <span class="apidocSignatureSpan">amqplib.callback_model.</span>Channel (connection)](#apidoc.element.amqplib.callback_model.Channel)
- description and source-code
```javascript
function Channel(connection) {
  BaseChannel.call(this, connection);
  this.on('delivery', this.handleDelivery.bind(this));
  this.on('cancel', this.handleCancel.bind(this));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.amqplib.callback_model.ConfirmChannel"></a>[function <span class="apidocSignatureSpan">amqplib.callback_model.</span>ConfirmChannel (connection)](#apidoc.element.amqplib.callback_model.ConfirmChannel)
- description and source-code
```javascript
function ConfirmChannel(connection) {
  Channel.call(this, connection);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.amqplib.channel"></a>[module amqplib.channel](#apidoc.module.amqplib.channel)

#### <a name="apidoc.element.amqplib.channel.BaseChannel"></a>[function <span class="apidocSignatureSpan">amqplib.channel.</span>BaseChannel (connection)](#apidoc.element.amqplib.channel.BaseChannel)
- description and source-code
```javascript
function BaseChannel(connection) {
  Channel.call(this, connection);
  this.consumers = {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.amqplib.channel.Channel"></a>[function <span class="apidocSignatureSpan">amqplib.channel.</span>Channel (connection)](#apidoc.element.amqplib.channel.Channel)
- description and source-code
```javascript
function Channel(connection) {
  EventEmitter.call( this );
  this.connection = connection;
  // for the presently outstanding RPC
  this.reply = null;
  // for the RPCs awaiting action
  this.pending = [];
  // for unconfirmed messages
  this.lwm = 1; // the least, unconfirmed deliveryTag
  this.unconfirmed = []; // rolling window of delivery callbacks
  this.on('ack', this.handleConfirm.bind(this, function(cb) {
    if (cb) cb(null);
  }));
  this.on('nack', this.handleConfirm.bind(this, function(cb) {
    if (cb) cb(new Error('message nacked'));
  }));
  // message frame state machine
  this.handleMessage = acceptDeliveryOrReturn;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.amqplib.channel.acceptMessage"></a>[function <span class="apidocSignatureSpan">amqplib.channel.</span>acceptMessage (continuation)](#apidoc.element.amqplib.channel.acceptMessage)
- description and source-code
```javascript
function acceptMessage(continuation) {
  var totalSize = 0, remaining = 0;
  var buffers = null;

  var message = {
    fields: null,
    properties: null,
    content: null
  };

  return headers;

  // expect a headers frame
  function headers(f) {
    if (f.id === defs.BasicProperties) {
      message.properties = f.fields;
      totalSize = remaining = f.size;

      // for zero-length messages, content frames aren't required.
      if (totalSize === 0) {
        message.content = new Buffer(0);
        continuation(message);
        return acceptDeliveryOrReturn;
      }
      else {
        return content;
      }
    }
    else {
      throw "Expected headers frame after delivery";
    }
  }

  // expect a content frame
  // %%% TODO cancelled messages (sent as zero-length content frame)
  function content(f) {
    if (f.content) {
      var size = f.content.length;
      remaining -= size;
      if (remaining === 0) {
        if (buffers !== null) {
          buffers.push(f.content);
          message.content = Buffer.concat(buffers);
        }
        else {
          message.content = f.content;
        }
        continuation(message);
        return acceptDeliveryOrReturn;
      }
      else if (remaining < 0) {
        throw fmt("Too much content sent! Expected %d bytes",
                  totalSize);
      }
      else {
        if (buffers !== null)
          buffers.push(f.content);
        else
          buffers = [f.content];
        return content;
      }
    }
    else throw "Expected content frame after headers"
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.amqplib.channel_model"></a>[module amqplib.channel_model](#apidoc.module.amqplib.channel_model)

#### <a name="apidoc.element.amqplib.channel_model.Channel"></a>[function <span class="apidocSignatureSpan">amqplib.channel_model.</span>Channel (connection)](#apidoc.element.amqplib.channel_model.Channel)
- description and source-code
```javascript
function Channel(connection) {
  BaseChannel.call(this, connection);
  this.on('delivery', this.handleDelivery.bind(this));
  this.on('cancel', this.handleCancel.bind(this));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.amqplib.channel_model.ChannelModel"></a>[function <span class="apidocSignatureSpan">amqplib.channel_model.</span>ChannelModel (connection)](#apidoc.element.amqplib.channel_model.ChannelModel)
- description and source-code
```javascript
function ChannelModel(connection) {
  if (!(this instanceof ChannelModel))
    return new ChannelModel(connection);
  EventEmitter.call( this );
  this.connection = connection;
  var self = this;
  ['error', 'close', 'blocked', 'unblocked'].forEach(function(ev) {
    connection.on(ev, self.emit.bind(self, ev));
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.amqplib.channel_model.ConfirmChannel"></a>[function <span class="apidocSignatureSpan">amqplib.channel_model.</span>ConfirmChannel (connection)](#apidoc.element.amqplib.channel_model.ConfirmChannel)
- description and source-code
```javascript
function ConfirmChannel(connection) {
  Channel.call(this, connection);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.amqplib.codec"></a>[module amqplib.codec](#apidoc.module.amqplib.codec)

#### <a name="apidoc.element.amqplib.codec.decodeFields"></a>[function <span class="apidocSignatureSpan">amqplib.codec.</span>decodeFields (slice)](#apidoc.element.amqplib.codec.decodeFields)
- description and source-code
```javascript
function decodeFields(slice) {
    var fields = {}, offset = 0, size = slice.length;
    var len, key, val;

    function decodeFieldValue() {
        var tag = String.fromCharCode(slice[offset]); offset++;
        switch (tag) {
        case 'b':
            val = slice.readInt8(offset); offset++;
            break;
        case 'S':
            len = slice.readUInt32BE(offset); offset += 4;
            val = slice.toString('utf8', offset, offset + len);
            offset += len;
            break;
        case 'I':
            val = slice.readInt32BE(offset); offset += 4;
            break;
        case 'D': // only positive decimals, apparently.
            var places = slice[offset]; offset++;
            var digits = slice.readUInt32BE(offset); offset += 4;
            val = {'!': 'decimal', value: {places: places, digits: digits}};
            break;
        case 'T':
            val = ints.readUInt64BE(slice, offset); offset += 8;
            val = {'!': 'timestamp', value: val};
            break;
        case 'F':
            len = slice.readUInt32BE(offset); offset += 4;
            val = decodeFields(slice.slice(offset, offset + len));
            offset += len;
            break;
        case 'A':
            len = slice.readUInt32BE(offset); offset += 4;
            decodeArray(offset + len);
            // NB decodeArray will itself update offset and val
            break;
        case 'd':
            val = slice.readDoubleBE(offset); offset += 8;
            break;
        case 'f':
            val = slice.readFloatBE(offset); offset += 4;
            break;
        case 'l':
            val = ints.readInt64BE(slice, offset); offset += 8;
            break;
        case 's':
            val = slice.readInt16BE(offset); offset += 2;
            break;
        case 't':
            val = slice[offset] != 0; offset++;
            break;
        case 'V':
            val = null;
            break;
        case 'x':
            len = slice.readUInt32BE(offset); offset += 4;
            val = slice.slice(offset, offset + len);
            offset += len;
            break;
        default:
            throw new TypeError('Unexpected type tag "' + tag +'"');
        }
    }

    function decodeArray(until) {
        var vals = [];
        while (offset < until) {
            decodeFieldValue();
            vals.push(val);
        }
        val = vals;
    }

    while (offset < size) {
        len = slice.readUInt8(offset); offset++;
        key = slice.toString('utf8', offset, offset + len);
        offset += len;
        decodeFieldValue();
        fields[key] = val;
    }
    return fields;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.amqplib.codec.encodeTable"></a>[function <span class="apidocSignatureSpan">amqplib.codec.</span>encodeTable (buffer, val, offset)](#apidoc.element.amqplib.codec.encodeTable)
- description and source-code
```javascript
function encodeTable(buffer, val, offset) {
    var start = offset;
    offset += 4; // leave room for the table length
    for (var key in val) {
        if (val[key] !== undefined) {
          var len = Buffer.byteLength(key);
          buffer.writeUInt8(len, offset); offset++;
          buffer.write(key, offset, 'utf8'); offset += len;
          offset += encodeFieldValue(buffer, val[key], offset);
        }
    }
    var size = offset - start;
    buffer.writeUInt32BE(size - 4, start);
    return size;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.amqplib.connect"></a>[module amqplib.connect](#apidoc.module.amqplib.connect)

#### <a name="apidoc.element.amqplib.connect.connect"></a>[function <span class="apidocSignatureSpan">amqplib.</span>connect (url, socketOptions, openCallback)](#apidoc.element.amqplib.connect.connect)
- description and source-code
```javascript
function connect(url, socketOptions, openCallback) {
  // tls.connect uses 'util._extend()' on the options given it, which
  // copies only properties mentioned in 'Object.keys()', when
  // processing the options. So I have to make copies too, rather
  // than using 'Object.create()'.
  var sockopts = clone(socketOptions || {});
  url = url || 'amqp://localhost';

  var noDelay = !!sockopts.noDelay;
  var timeout = sockopts.timeout;
  var keepAlive = !!sockopts.keepAlive;
  // 0 is default for node
  var keepAliveDelay = sockopts.keepAliveDelay || 0;

  var extraClientProperties = sockopts.clientProperties || {};

  var protocol, fields;
  if (typeof url === 'object') {
    protocol = (url.protocol || 'amqp') + ':';
    sockopts.host = url.hostname;
    sockopts.port = url.port || ((protocol === 'amqp:') ? 5672 : 5671);

    var user, pass;
    if (!url.username) {
      user = 'guest';
      pass = url.password || 'guest';
    } else {
      user = url.username;
      pass = url.password;
    }

    fields = openFrames(url.vhost, null, sockopts.credentials || credentials.plain(user, pass), extraClientProperties);
  } else {
    var parts = URL.parse(url, true); // yes, parse the query string
    protocol = parts.protocol;
    sockopts.host = parts.hostname;
    sockopts.port = parseInt(parts.port) || ((protocol === 'amqp:') ? 5672 : 5671);
    var vhost = parts.pathname ? parts.pathname.substr(1) : null;
    fields = openFrames(vhost, parts.query, sockopts.credentials || credentialsFromUrl(parts), extraClientProperties);
  }

  var sockok = false;
  var sock;

  function onConnect() {
    sockok = true;
    sock.setNoDelay(noDelay);
    if (keepAlive) sock.setKeepAlive(keepAlive, keepAliveDelay);

    var c = new Connection(sock);
    c.open(fields, function(err, ok) {
      // disable timeout once the connection is open, we don't want
      // it fouling things
      if (timeout) sock.setTimeout(0);
      if (err === null) {
        openCallback(null, c);
      }
      else openCallback(err);
    });
  }

  if (protocol === 'amqp:') {
    sock = require('net').connect(sockopts, onConnect);
  }
  else if (protocol === 'amqps:') {
    sock = require('tls').connect(sockopts, onConnect);
  }
  else {
    throw new Error("Expected amqp: or amqps: as the protocol; got " + protocol);
  }

  if (timeout) {
    sock.setTimeout(
      timeout, openCallback.bind(this, new Error('connect ETIMEDOUT')));
  }

  sock.once('error', function(err) {
    if (!sockok) openCallback(err);
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



# <a name="apidoc.module.amqplib.connection"></a>[module amqplib.connection](#apidoc.module.amqplib.connection)

#### <a name="apidoc.element.amqplib.connection.Connection"></a>[function <span class="apidocSignatureSpan">amqplib.connection.</span>Connection (underlying)](#apidoc.element.amqplib.connection.Connection)
- description and source-code
```javascript
function Connection(underlying) {
  EventEmitter.call( this );
  var stream = this.stream = wrapStream(underlying);
  this.muxer = new Mux(stream);

  // frames
  this.rest = new Buffer(0);
  this.frameMax = constants.FRAME_MIN_SIZE;
  this.sentSinceLastCheck = false;
  this.recvSinceLastCheck = false;

  this.expectSocketClose = false;
  this.freeChannels = new BitSet();
  this.channels = [{channel: {accept: channel0(this)},
                    buffer: underlying}];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.amqplib.connection.isFatalError"></a>[function <span class="apidocSignatureSpan">amqplib.connection.</span>isFatalError (error)](#apidoc.element.amqplib.connection.isFatalError)
- description and source-code
```javascript
function isFatalError(error) {
  switch (error && error.code) {
  case defs.constants.CONNECTION_FORCED:
  case defs.constants.REPLY_SUCCESS:
    return false;
  default:
    return true;
  }
}
```
- example usage
```shell
n/a
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
...
function credentialsFromUrl(parts) {
var user = 'guest', passwd = 'guest';
if (parts.auth) {
  var auth = parts.auth.split(':');
  user = auth[0];
  passwd = auth[1];
}
return credentials.plain(user, passwd);
}

function connect(url, socketOptions, openCallback) {
// tls.connect uses 'util._extend()' on the options given it, which
// copies only properties mentioned in 'Object.keys()', when
// processing the options. So I have to make copies too, rather
// than using 'Object.create()'.
...
```



# <a name="apidoc.module.amqplib.defs"></a>[module amqplib.defs](#apidoc.module.amqplib.defs)

#### <a name="apidoc.element.amqplib.defs.decode"></a>[function <span class="apidocSignatureSpan">amqplib.defs.</span>decode (id, buf)](#apidoc.element.amqplib.defs.decode)
- description and source-code
```javascript
decode = function (id, buf) {
  switch (id) {
   case 655370:
    return decodeConnectionStart(buf);

   case 655371:
    return decodeConnectionStartOk(buf);

   case 655380:
    return decodeConnectionSecure(buf);

   case 655381:
    return decodeConnectionSecureOk(buf);

   case 655390:
    return decodeConnectionTune(buf);

   case 655391:
    return decodeConnectionTuneOk(buf);

   case 655400:
    return decodeConnectionOpen(buf);

   case 655401:
    return decodeConnectionOpenOk(buf);

   case 655410:
    return decodeConnectionClose(buf);

   case 655411:
    return decodeConnectionCloseOk(buf);

   case 655420:
    return decodeConnectionBlocked(buf);

   case 655421:
    return decodeConnectionUnblocked(buf);

   case 1310730:
    return decodeChannelOpen(buf);

   case 1310731:
    return decodeChannelOpenOk(buf);

   case 1310740:
    return decodeChannelFlow(buf);

   case 1310741:
    return decodeChannelFlowOk(buf);

   case 1310760:
    return decodeChannelClose(buf);

   case 1310761:
    return decodeChannelCloseOk(buf);

   case 1966090:
    return decodeAccessRequest(buf);

   case 1966091:
    return decodeAccessRequestOk(buf);

   case 2621450:
    return decodeExchangeDeclare(buf);

   case 2621451:
    return decodeExchangeDeclareOk(buf);

   case 2621460:
    return decodeExchangeDelete(buf);

   case 2621461:
    return decodeExchangeDeleteOk(buf);

   case 2621470:
    return decodeExchangeBind(buf);

   case 2621471:
    return decodeExchangeBindOk(buf);

   case 2621480:
    return decodeExchangeUnbind(buf);

   case 2621491:
    return decodeExchangeUnbindOk(buf);

   case 3276810:
    return decodeQueueDeclare(buf);

   case 3276811:
    return decodeQueueDeclareOk(buf);

   case 3276820:
    return decodeQueueBind(buf);

   case 3276821:
    return decodeQueueBindOk(buf);

   case 3276830:
    return decodeQueuePurge(buf);

   case 3276831:
    return decodeQueuePurgeOk(buf);

   case 3276840:
    return decodeQueueDelete(buf);

   case 3276841:
    return decodeQueueDeleteOk(buf);

   case 3276850:
    return decodeQueueUnbind(buf);

   case 3276851:
    return decodeQueueUnbindOk(buf);

   case 3932170:
    return decodeBasicQos(buf);

   case 3932171:
    return decodeBasicQosOk(buf);

   case 3932180:
    return decodeBasicConsume(buf);

   case 3932181:
    return decodeBasicConsumeOk(buf);

   case 3932190:
    return decodeBasicCancel(buf);

   case 3932191:
    return decodeBasicCancelOk(buf);

   case 3932200:
    return decodeBasicPublish(buf);

   case 3932210:
    return decodeBasicReturn(buf);

   case 3932220:
    return decodeBasicDeliver(buf);

   case 3932230:
    return decodeBasicGet(buf);

   case 3932231:
    return decodeBasicGetOk(buf);

   case 3932232:
    return decodeBasicGetEmpty(buf);

   case 3932240:
    return decodeBasicAck(buf);

   case 3932250:
    return decodeBasicReject(buf);

   case 3932260:
    return decodeBasicRecoverAsync(buf);

   case 3932270:
    return decodeBasicRecover(buf);

   case 3932271:
    return decodeBasicRecoverOk(buf);

   case 3932280:
    return decodeBasicNack(buf);

   case 5898250:
    return decodeTxSelect(buf);

   case 5898251:
    return decodeTxSelectOk(buf);

   case 5898260:
    return decodeTxCommit(buf);

   case 5898261:
    return decodeTxCommitOk(buf);

   case 5898270:
    return decodeTxRollback(buf);

   case 5898271:
    return decodeTxRollbackOk(buf);

   case 5570570:
    return decodeConfirmSelect(buf);

   case 5570571:
    return decodeConfirmSelectOk(buf);

   case 60:
    return decodeBasicProperties(buf);

   default:
    throw new Error("Unknown class/method ID");
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.amqplib.defs.encodeMethod"></a>[function <span class="apidocSignatureSpan">amqplib.defs.</span>encodeMethod (id, channel, fields)](#apidoc.element.amqplib.defs.encodeMethod)
- description and source-code
```javascript
encodeMethod = function (id, channel, fields) {
  switch (id) {
   case 655370:
    return encodeConnectionStart(channel, fields);

   case 655371:
    return encodeConnectionStartOk(channel, fields);

   case 655380:
    return encodeConnectionSecure(channel, fields);

   case 655381:
    return encodeConnectionSecureOk(channel, fields);

   case 655390:
    return encodeConnectionTune(channel, fields);

   case 655391:
    return encodeConnectionTuneOk(channel, fields);

   case 655400:
    return encodeConnectionOpen(channel, fields);

   case 655401:
    return encodeConnectionOpenOk(channel, fields);

   case 655410:
    return encodeConnectionClose(channel, fields);

   case 655411:
    return encodeConnectionCloseOk(channel, fields);

   case 655420:
    return encodeConnectionBlocked(channel, fields);

   case 655421:
    return encodeConnectionUnblocked(channel, fields);

   case 1310730:
    return encodeChannelOpen(channel, fields);

   case 1310731:
    return encodeChannelOpenOk(channel, fields);

   case 1310740:
    return encodeChannelFlow(channel, fields);

   case 1310741:
    return encodeChannelFlowOk(channel, fields);

   case 1310760:
    return encodeChannelClose(channel, fields);

   case 1310761:
    return encodeChannelCloseOk(channel, fields);

   case 1966090:
    return encodeAccessRequest(channel, fields);

   case 1966091:
    return encodeAccessRequestOk(channel, fields);

   case 2621450:
    return encodeExchangeDeclare(channel, fields);

   case 2621451:
    return encodeExchangeDeclareOk(channel, fields);

   case 2621460:
    return encodeExchangeDelete(channel, fields);

   case 2621461:
    return encodeExchangeDeleteOk(channel, fields);

   case 2621470:
    return encodeExchangeBind(channel, fields);

   case 2621471:
    return encodeExchangeBindOk(channel, fields);

   case 2621480:
    return encodeExchangeUnbind(channel, fields);

   case 2621491:
    return encodeExchangeUnbindOk(channel, fields);

   case 3276810:
    return encodeQueueDeclare(channel, fields);

   case 3276811:
    return encodeQueueDeclareOk(channel, fields);

   case 3276820:
    return encodeQueueBind(channel, fields);

   case 3276821:
    return encodeQueueBindOk(channel, fields);

   case 3276830:
    return encodeQueuePurge(channel, fields);

   case 3276831:
    return encodeQueuePurgeOk(channel, fields);

   case 3276840:
    return encodeQueueDelete(channel, fields);

   case 3276841:
    return encodeQueueDeleteOk(channel, fields);

   case 3276850:
    return encodeQueueUnbind(channel, fields);

   case 3276851:
    return encodeQueueUnbindOk(channel, fields);

   case 3932170:
    return encodeBasicQos(channel, fields);

   case 3932171:
    return encodeBasicQosOk(channel, fields);

   case 3932180:
    return encodeBasicConsume(channel, fields);

   case 3932181:
    return encodeBasicConsumeOk(channel, fields);

   case 3932190:
    return encodeBasicCancel(channel, fields);

   case 3932191:
    return encodeBasicCancelOk(channel, fields);

   case 3932200:
    return encodeBasicPublish(channel, fields);

   case 3932210:
    return encodeBasicReturn(channel, fields);

   case 3932220:
    return encodeBasicDeliver(channel, fields);

   case 3932230:
    return encodeBasicGet(channel, fields);

   case 3932231:
    return encodeBasicGetOk(channel, fields);

   case 3932232:
    return encodeBasicGetEmpty(channel, fields);

   case 3932240:
    return encodeBasicAck(channel, fields);

   case 3932250:
    return encodeBasicReject(channel, fields);

   case 3932260:
    return encodeBasicRecoverAsync(channel, fields);

   case 3932270:
    return encodeBasicRecover(channel, fields);

   case 3932271:
    return encodeBasicRecoverOk(channel, fields);

   case 3932280:
    return encodeBasicNack(channel, fields);

   case 5898250:
    return encodeTxSelect(channel, fields);

   case 5898251:
    return encodeTxSelectOk(channel, fields);

   case 5898260:
    return encodeTxCommit(channel, fields);

   case 5898261:
    return encodeTxCommitOk(channel, fields);

   case 5898270:
    return encodeTxRollback(cha ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.amqplib.defs.encodeProperties"></a>[function <span class="apidocSignatureSpan">amqplib.defs.</span>encodeProperties (id, channel, size, fields)](#apidoc.element.amqplib.defs.encodeProperties)
- description and source-code
```javascript
encodeProperties = function (id, channel, size, fields) {
  switch (id) {
   case 60:
    return encodeBasicProperties(channel, size, fields);

   default:
    throw new Error("Unknown class/properties ID");
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.amqplib.defs.info"></a>[function <span class="apidocSignatureSpan">amqplib.defs.</span>info (id)](#apidoc.element.amqplib.defs.info)
- description and source-code
```javascript
info = function (id) {
  switch (id) {
   case 655370:
    return methodInfoConnectionStart;

   case 655371:
    return methodInfoConnectionStartOk;

   case 655380:
    return methodInfoConnectionSecure;

   case 655381:
    return methodInfoConnectionSecureOk;

   case 655390:
    return methodInfoConnectionTune;

   case 655391:
    return methodInfoConnectionTuneOk;

   case 655400:
    return methodInfoConnectionOpen;

   case 655401:
    return methodInfoConnectionOpenOk;

   case 655410:
    return methodInfoConnectionClose;

   case 655411:
    return methodInfoConnectionCloseOk;

   case 655420:
    return methodInfoConnectionBlocked;

   case 655421:
    return methodInfoConnectionUnblocked;

   case 1310730:
    return methodInfoChannelOpen;

   case 1310731:
    return methodInfoChannelOpenOk;

   case 1310740:
    return methodInfoChannelFlow;

   case 1310741:
    return methodInfoChannelFlowOk;

   case 1310760:
    return methodInfoChannelClose;

   case 1310761:
    return methodInfoChannelCloseOk;

   case 1966090:
    return methodInfoAccessRequest;

   case 1966091:
    return methodInfoAccessRequestOk;

   case 2621450:
    return methodInfoExchangeDeclare;

   case 2621451:
    return methodInfoExchangeDeclareOk;

   case 2621460:
    return methodInfoExchangeDelete;

   case 2621461:
    return methodInfoExchangeDeleteOk;

   case 2621470:
    return methodInfoExchangeBind;

   case 2621471:
    return methodInfoExchangeBindOk;

   case 2621480:
    return methodInfoExchangeUnbind;

   case 2621491:
    return methodInfoExchangeUnbindOk;

   case 3276810:
    return methodInfoQueueDeclare;

   case 3276811:
    return methodInfoQueueDeclareOk;

   case 3276820:
    return methodInfoQueueBind;

   case 3276821:
    return methodInfoQueueBindOk;

   case 3276830:
    return methodInfoQueuePurge;

   case 3276831:
    return methodInfoQueuePurgeOk;

   case 3276840:
    return methodInfoQueueDelete;

   case 3276841:
    return methodInfoQueueDeleteOk;

   case 3276850:
    return methodInfoQueueUnbind;

   case 3276851:
    return methodInfoQueueUnbindOk;

   case 3932170:
    return methodInfoBasicQos;

   case 3932171:
    return methodInfoBasicQosOk;

   case 3932180:
    return methodInfoBasicConsume;

   case 3932181:
    return methodInfoBasicConsumeOk;

   case 3932190:
    return methodInfoBasicCancel;

   case 3932191:
    return methodInfoBasicCancelOk;

   case 3932200:
    return methodInfoBasicPublish;

   case 3932210:
    return methodInfoBasicReturn;

   case 3932220:
    return methodInfoBasicDeliver;

   case 3932230:
    return methodInfoBasicGet;

   case 3932231:
    return methodInfoBasicGetOk;

   case 3932232:
    return methodInfoBasicGetEmpty;

   case 3932240:
    return methodInfoBasicAck;

   case 3932250:
    return methodInfoBasicReject;

   case 3932260:
    return methodInfoBasicRecoverAsync;

   case 3932270:
    return methodInfoBasicRecover;

   case 3932271:
    return methodInfoBasicRecoverOk;

   case 3932280:
    return methodInfoBasicNack;

   case 5898250:
    return methodInfoTxSelect;

   case 5898251:
    return methodInfoTxSelectOk;

   case 5898260:
    return methodInfoTxCommit;

   case 5898261:
    return methodInfoTxCommitOk;

   case 5898270:
    return methodInfoTxRollback;

   case 5898271:
    return methodInfoTxRollbackOk;

   case 5570570:
    return methodInfoConfirmSelect;

   case 5570571:
    return methodInfoConfirmSelectOk;

   case 60:
    return propertiesInfoBasicProperties;

   default:
    throw new Error("Unknown class/method ID");
  }
}
```
- example usage
```shell
...
var code = close.fields.replyCode;
return format('%d (%s) with message "%s"',
              code, defs.constant_strs[code],
              close.fields.replyText);
}

module.exports.methodName = function(id) {
return defs.info(id).name;
};

module.exports.inspect = function(frame, showFields) {
if (frame === HEARTBEAT) {
  return '<Heartbeat>';
}
else if (!frame.id) {
...
```



# <a name="apidoc.module.amqplib.error"></a>[module amqplib.error](#apidoc.module.amqplib.error)

#### <a name="apidoc.element.amqplib.error.IllegalOperationError"></a>[function <span class="apidocSignatureSpan">amqplib.error.</span>IllegalOperationError (msg, stack)](#apidoc.element.amqplib.error.IllegalOperationError)
- description and source-code
```javascript
function IllegalOperationError(msg, stack) {
  var tmp = new Error();
  this.message = msg;
  this.stack = this.toString() + '\n' + trimStack(tmp.stack, 2);
  this.stackAtStateChange = stack;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.amqplib.error.stackCapture"></a>[function <span class="apidocSignatureSpan">amqplib.error.</span>stackCapture (reason)](#apidoc.element.amqplib.error.stackCapture)
- description and source-code
```javascript
function stackCapture(reason) {
  var e = new Error();
  return 'Stack capture: ' + reason + '\n' +
    trimStack(e.stack, 2);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.amqplib.format"></a>[module amqplib.format](#apidoc.module.amqplib.format)

#### <a name="apidoc.element.amqplib.format.closeMessage"></a>[function <span class="apidocSignatureSpan">amqplib.format.</span>closeMessage (close)](#apidoc.element.amqplib.format.closeMessage)
- description and source-code
```javascript
closeMessage = function (close) {
  var code = close.fields.replyCode;
  return format('%d (%s) with message "%s"',
                code, defs.constant_strs[code],
                close.fields.replyText);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.amqplib.format.inspect"></a>[function <span class="apidocSignatureSpan">amqplib.format.</span>inspect (frame, showFields)](#apidoc.element.amqplib.format.inspect)
- description and source-code
```javascript
inspect = function (frame, showFields) {
  if (frame === HEARTBEAT) {
    return '<Heartbeat>';
  }
  else if (!frame.id) {
    return format('<Content channel:%d size:%d>',
                  frame.channel, frame.size);
  }
  else {
    var info = defs.info(frame.id);
    return format('<%s channel:%d%s>', info.name, frame.channel,
                  (showFields)
                  ? ' ' + JSON.stringify(frame.fields, undefined, 2)
                  : '');
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.amqplib.format.methodName"></a>[function <span class="apidocSignatureSpan">amqplib.format.</span>methodName (id)](#apidoc.element.amqplib.format.methodName)
- description and source-code
```javascript
methodName = function (id) {
  return defs.info(id).name;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.amqplib.frame"></a>[module amqplib.frame](#apidoc.module.amqplib.frame)

#### <a name="apidoc.element.amqplib.frame.decodeFrame"></a>[function <span class="apidocSignatureSpan">amqplib.frame.</span>decodeFrame (frame)](#apidoc.element.amqplib.frame.decodeFrame)
- description and source-code
```javascript
decodeFrame = function (frame) {
  var payload = frame.payload;
  switch (frame.type) {
  case FRAME_METHOD:
    var idAndArgs = methodPattern(payload);
    var id = idAndArgs.id;
    var fields = decode(id, idAndArgs.args);
    return {id: id, channel: frame.channel, fields: fields};
  case FRAME_HEADER:
    var parts = headerPattern(payload);
    var id = parts['class'];
    var fields = decode(id, parts.flagsAndfields);
    return {id: id, channel: frame.channel,
            size: parts.size, fields: fields};
  case FRAME_BODY:
    return {channel: frame.channel, content: frame.payload};
  case FRAME_HEARTBEAT:
    return HEARTBEAT;
  default:
    throw new Error('Unknown frame type ' + frame.type);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.amqplib.frame.makeBodyFrame"></a>[function <span class="apidocSignatureSpan">amqplib.frame.</span>makeBodyFrame (channel, payload)](#apidoc.element.amqplib.frame.makeBodyFrame)
- description and source-code
```javascript
makeBodyFrame = function (channel, payload) {
  return bodyCons({channel: channel, size: payload.length, payload: payload});
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.amqplib.frame.parseFrame"></a>[function <span class="apidocSignatureSpan">amqplib.frame.</span>parseFrame (bin, max)](#apidoc.element.amqplib.frame.parseFrame)
- description and source-code
```javascript
function parseFrame(bin, max) {
  var fh = frameHeaderPattern(bin);
  if (fh) {
    var size = fh.size, rest = fh.rest;
    if (size > max) {
      throw new Error('Frame size exceeds frame max');
    }
    else if (rest.length > size) {
      if (rest[size] !== FRAME_END)
        throw new Error('Invalid frame');

      return {
        type: fh.type,
        channel: fh.channel,
        size: size,
        payload: rest.slice(0, size),
        rest: rest.slice(size + 1)
      };
    }
  }
  return false;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.amqplib.heartbeat"></a>[module amqplib.heartbeat](#apidoc.module.amqplib.heartbeat)

#### <a name="apidoc.element.amqplib.heartbeat.Heart"></a>[function <span class="apidocSignatureSpan">amqplib.heartbeat.</span>Heart (interval, checkSend, checkRecv)](#apidoc.element.amqplib.heartbeat.Heart)
- description and source-code
```javascript
function Heart(interval, checkSend, checkRecv) {
  EventEmitter.call(this);
  this.interval = interval;

  var intervalMs = interval * module.exports.UNITS_TO_MS;
  // Function#bind is my new best friend
  var beat = this.emit.bind(this, 'beat');
  var timeout = this.emit.bind(this, 'timeout');

  this.sendTimer = setInterval(
    this.runHeartbeat.bind(this, checkSend, beat), intervalMs / 2);

  // A timeout occurs if I see nothing for *two consecutive* intervals
  var recvMissed = 0;
  function missedTwo() {
    if (!checkRecv()) return (++recvMissed < 2);
    else { recvMissed = 0; return true; }
  }
  this.recvTimer = setInterval(
    this.runHeartbeat.bind(this, missedTwo, timeout), intervalMs);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.amqplib.mux"></a>[module amqplib.mux](#apidoc.module.amqplib.mux)

#### <a name="apidoc.element.amqplib.mux.Mux"></a>[function <span class="apidocSignatureSpan">amqplib.mux.</span>Mux (downstream)](#apidoc.element.amqplib.mux.Mux)
- description and source-code
```javascript
function Mux(downstream) {
  this.newStreams = [];
  this.oldStreams = [];
  this.blocked = false;
  this.scheduledRead = false;

  this.out = downstream;
  var self = this;
  downstream.on('drain', function() {
    self.blocked = false;
    self._readIncoming();
  });
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
