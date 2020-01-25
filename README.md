# gommand

A simple way to define multiple applications in the same command.

## Usage

```go
package main

import (
    "gitlab.com/getlytica/golog"
    "gitlab.com/getlytica/gommand"
    "gitlab.com/getlytica/example/monitoring"
    "gitlab.com/getlytica/example/research"
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
