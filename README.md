# gommand

A simple way to define multiple applications in the same command.

## Usage

```go
package main

import (
    "gitlab.com/lyticaa-public/golog"
    "gitlab.com/lyticaa-public/gommand"
    "gitlab.com/lyticaa-public/example/monitoring"
    "gitlab.com/lyticaa-public/example/research"
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
