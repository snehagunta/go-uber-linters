# go-uber-linters

Reusable Go analysis passes for domain modeling rules, built on `golang.org/x/tools/go/analysis`.

The `domainconstruct` package exports three analyzers:

- `Analyzer` checks approved construction and protected domain state.
- `ZeroAnalyzer` detects invalid zero-value flows.
- `SerializationAnalyzer` checks declared serialization contracts and plain snapshots.

Types opt into checks with `domain:*` directives in their Go doc comments. See the package documentation and analyzer tests for supported directives and behavior.

## Installation

```sh
go get github.com/snehagunta/go-uber-linters@v0.1.0
```

A custom analyzer runner can import the analyzers directly:

```go
import "github.com/snehagunta/go-uber-linters/domainconstruct"
```

The library is distributed under the Apache-2.0 license.
