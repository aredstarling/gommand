# gommand

A simple way to define multiple applications in the same command.

## Usage

```go
package main

import (
    "gitlab.com/aredstarling/golog"
    "gitlab.com/aredstarling/gommand"
    "gitlab.com/aredstarling/example/monitoring"
    "gitlab.com/aredstarling/example/research"
)

func main() {
    logger := golog.CreateStdout()
    applications := []gommand.Application{
        research.CreateApplication(),
        monitoring.CreateApplication(),
    }

    gommand.StartApplications(logger, applications)
}
```
