## Dep
 Some consider `go modules` is kosher. Others use a custom dependency management tool for Golang. But if you use third-party libraries, you must obey the choice of the another developer regarding this (probably gophers love pain).

[Dep](https://golang.github.io/dep/) is a dependency management tool for Go that requires Go 1.9 or newer to compile.
Since there's no appropriate version of Go for some Linux distributives, `dep init` does not write out a partial Gopkg.toml when it fails. 

Removing functions `ValidateProjectRoots` and `ValidateParams` and rebuilding dep fixed the issue in my case (it is described [here](https://github.com/golang/dep/issues/909)) 

## Installation

```sh
$ curl https://raw.githubusercontent.com/alissiawells/dep/master/install.sh | sh
```

It will install into your `$GOPATH/bin` directory by default or any other directory you specify using the `INSTALL_DIRECTORY` environment variable.
`
