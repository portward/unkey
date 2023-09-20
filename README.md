# Unkey authenticator

[![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/portward/unkey-authenticator/ci.yaml?style=flat-square)](https://github.com/portward/unkey-authenticator/actions/workflows/ci.yaml)
[![go.dev reference](https://img.shields.io/badge/go.dev-reference-007d9c?logo=go&logoColor=white&style=flat-square)](https://pkg.go.dev/mod/github.com/portward/unkey-authenticator)
[![built with nix](https://img.shields.io/badge/builtwith-nix-7d81f7?style=flat-square)](https://builtwithnix.org)

**Authenticate API keys using [Unkey](https://unkey.dev).**

> [!WARNING]
> **Project is under development. Backwards compatibility is not guaranteed.**

## Development

**For an optimal developer experience, it is recommended to install [Nix](https://nixos.org/download.html) and [direnv](https://direnv.net/docs/installation.html).**

Run tests:

```shell
go test -race -v ./...
```

Run linter:

```shell
golangci-lint run
```

To test changes made in [registry-auth](https://github.com/portward/registry-auth) and [registry-auth-config](https://github.com/portward/registry-auth-config):

Make sure [registry-auth](https://github.com/portward/registry-auth) and [registry-auth-config](https://github.com/portward/registry-auth-config) are checked out in the same directory:

```shell
cd ..
git clone git@github.com:portward/registry-auth.git
git clone git@github.com:portward/registry-auth-config.git
cd unkey-authenticator
```

Set up a Go workspace:

```shell
go work init
go work use .
go work use ../registry-auth
go work use ../registry-auth-config
go work sync
```

## License

The project is licensed under the [MIT License](LICENSE).
