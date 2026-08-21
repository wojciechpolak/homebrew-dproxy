# homebrew-dproxy

A [Homebrew](https://brew.sh) tap for
[dproxy](https://github.com/wojciechpolak/dproxy), a discreet encrypted proxy
for HTTPS and WebSocket traffic.

## Install

```sh
brew install wojciechpolak/dproxy/dproxy
```

That command taps this repository and installs the macOS or Linux binary for
the host architecture.

## Upgrade and uninstall

```sh
brew upgrade wojciechpolak/dproxy/dproxy
brew uninstall wojciechpolak/dproxy/dproxy
brew untap wojciechpolak/dproxy
```

Homebrew does not remove files under `~/.config/dproxy` during an upgrade or
uninstall.

## What gets installed

The formula selects the macOS or Linux arm64 or amd64 archive from the matching
dproxy release. Homebrew checks the archive's SHA-256 digest before
installation. The main project also publishes signed GitHub build provenance
for the same archive.

Installing the client does not deploy a remote relay. Follow the
[dproxy deployment guide](https://github.com/wojciechpolak/dproxy/blob/master/docs/deployment.md)
to run the server behind Cloudflare Tunnel, then configure the local client.

Client, protocol, and deployment issues belong in the
[dproxy issue tracker](https://github.com/wojciechpolak/dproxy/issues). Use this
repository only for packaging problems.

## About `Formula/dproxy.rb`

The formula is generated. A stable dproxy release renders it from the release
tag and platform archive checksums, tests it, and replaces the copy in this tap.
Edit the
[`render-homebrew-formula.sh`](https://github.com/wojciechpolak/dproxy/blob/master/scripts/render-homebrew-formula.sh)
script in the main repository instead of editing the formula here.

CI checks the formula with Homebrew on macOS and Linux, runs its offline
diagnostic test, and confirms the installed version.

## License

MIT, matching dproxy itself. See [LICENSE](LICENSE).
