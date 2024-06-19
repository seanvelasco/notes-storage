Package `main` has an entry point `main()` function. All other packages are library packages, and have no entry point. Libraries simply export functionality that can be used in other packages.

### Naming convention

By convention, the package name is the same as the last element of if import path. For example, the `math/rand` package comprises Go files that begin with

```go
package rand
```

However, package names aren't required to match their import that. For example, a package `github.com/seanvelasco/rand` named package `random`

```go
package random
```

While the above is possible, it is discouraged.

## Modules

Go programs are organized into packages. A package is a directory of Go code compiled together. Functions, types, variables, and constants defined in one source file are visible to other source files within the same package (directory).

A repository contains one or more modules. A module is a collection of Go packages released together.

A Go repository typically contains only one module, located at the root of the repository.

A file named `go.mod` at the root of the project declared the module. It contains:
- the module path
- the version of the Go language the project requires
- External package dependencies the project has

Example of a `go.mod`
```go
module github.com/seanvelasco/example

go 1.22.1

require github.com/google/example v1.3.0
```

The import path is a string used to import a package. A package import path is its module path joined with its subdirectory within the module. For example, the module `github.com/google/go-cmp` contains a package in the directory `/cmp`. The package's import path is `github.com/google/go-cmp/cmp`.

Packages in the standard library do not have a module path prefix.









By convention, package names are are the same as the directory

If we want to expose this function outside the package, we should capitalize the first letter of the function


### Custom package

In `go.mod`
```go
module example.com/username/hellogo

go 1.22.1

replace example.com/username/mystrings v0.0.0 => ../mystrings

require (
	example.com/username/mystrings v0.0.0
)
```

_Note: `../mystrings` means look in the parent directory of `hellogo` for the `mystrings` sibling directory._


Be aware that using the "replace" keyword like we did in the last assignment _isn't advised_, but can be useful to get up and running quickly. The _proper_ way to create and depend on modules is to publish them to a remote repository. When you do that, the "replace" keyword can be dropped from the `go.mod`:

### Bad

This works for local-only development

```go
module github.com/wagslane/hellogo

go 1.22.1

replace github.com/wagslane/mystrings v0.0.0 => ../mystrings

require (
	github.com/wagslane/mystrings v0.0.0
)
```

### Good

This works if we publish our modules to a remote location like [GitHub](https://github.com) as we should.

```go
module github.com/wagslane/hellogo

go 1.22.1

require (
	github.com/wagslane/mystrings v0.0.0
)
```


### Clean packages

1. Hide internal logic. Only expose functions that the application-level needs to know about.
2. Don't change API's to prevent breaking changes. Unexported functions can change. But exported functions' signature should not change.
3. Don't export functions from the main() package because it's not a library
4. Package should not know about its dependents. It should not have specific knowledge about a particular application that uses it
