# @servicebus/express
[![Build Status](https://travis-ci.org/servicebus/express.svg?branch=master)](https://travis-ci.org/servicebus/express)
[![codecov](https://codecov.io/gh/servicebus/express/branch/master/graph/badge.svg)](https://codecov.io/gh/servicebus/express)

express server configured with servicebus middleware, Prometheus exporters, and request (leveled optional) logging

## Usage

```
import log from 'llog'
import makeServer from '@servicebus/express'

const options = {
  logger: log
}
const server = makeServer(options)
server.use('/', () => { 
  //... 
})
server.start(PORT, onServerListen)
```