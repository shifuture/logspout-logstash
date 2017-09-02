[![GoDoc](https://godoc.org/github.com/looplab/logspout-logstash?status.svg)](https://godoc.org/github.com/looplab/logspout-logstash)
[![Go Report Card](https://goreportcard.com/badge/looplab/logspout-logstash)](https://goreportcard.com/report/looplab/logspout-logstash)

# logspout-logstash

Minor modification add multiline support

A minimalistic adapter for github.com/gliderlabs/logspout to write to Logstash

Follow the instructions in https://github.com/gliderlabs/logspout/tree/master/custom on how to build your own Logspout container with custom modules. Basically just copy the contents of the custom folder and include:

```go
package main

import (
        _ "github.com/shifuture/logspout-logstash-1"
        _ "github.com/gliderlabs/logspout/adapters/syslog"
        _ "github.com/gliderlabs/logspout/transports/tcp"
        _ "github.com/gliderlabs/logspout/transports/tls"
        _ "github.com/gliderlabs/logspout/transports/udp"
)
```

in modules.go.

Thanks for Goodbaby develop teams's direction, especially Kai &amp; Jun. Feel free to show me the error.

