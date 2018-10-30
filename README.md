<p align="center"><img src="docs/assets/DigbyShadows.png" width="360"></p>
<p align="center">
  <a href="https://travis-ci.org/golang/dep"><img src="https://travis-ci.org/golang/dep.svg?branch=master" alt="Build Status"></img></a>
  <a href="https://ci.appveyor.com/project/golang/dep"><img src="https://ci.appveyor.com/api/projects/status/github/golang/dep?svg=true&branch=master&passingText=Windows%20-%20OK&failingText=Windows%20-%20failed&pendingText=Windows%20-%20pending" alt="Windows Build Status"></a>
  <a href="https://goreportcard.com/report/github.com/golang/dep"><img src="https://goreportcard.com/badge/github.com/golang/dep" /></a>
</p>

## Dep
 Some consider `go modules` is kosher. Others use a custom dependency management tool for Golang. But if you use third-party libraries, you must obey the choice of the another developer regarding this.

[Dep](https://golang.github.io/dep/) is a dependency management tool for Go that requires Go 1.9 or newer to compile.
Since there's no appropriate version of Go for some Linux distributives, `dep init` does not write out a partial Gopkg.toml when it fails. 

Removing functions `ValidateProjectRoots` and `ValidateParams` and rebuilding dep fixed the issue in my case (it is described [here](https://github.com/golang/dep/issues/909)) 

## Installation

```sh
$ curl https://raw.githubusercontent.com/alissiawells/dep/master/install.sh | sh
```

It will install into your `$GOPATH/bin` directory by default or any other directory you specify using the `INSTALL_DIRECTORY` environment variable.
`
