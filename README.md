# gommand

A simple way to define multiple applications in the same command.

## Usage

```go
package main

import (
    "github.com/sellernomics/golog"
    "github.com/sellernomics/gommand"
    "github.com/sellernomics/example/monitoring"
    "github.com/sellernomics/example/research"
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
