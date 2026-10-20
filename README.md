# retrofit

[![release](https://img.shields.io/github/v/release/MonotonicHQ/retrofit?display_name=release&label=release)](https://github.com/MonotonicHQ/retrofit/releases/latest)
[![wip](https://img.shields.io/github/v/release/MonotonicHQ/retrofit?include_prereleases&display_name=release&label=wip)](https://github.com/MonotonicHQ/retrofit/releases)
[![PostgreSQL 15 to 18](https://img.shields.io/badge/PostgreSQL-15%20to%2018-336791)](#install)
[![macOS, Linux](https://img.shields.io/badge/platform-macOS%2C%20Linux-lightgrey)](#install)
[![license: binary only](https://img.shields.io/badge/license-binary%20only-lightgrey)](LICENSE)
[![chat on Discord](https://img.shields.io/badge/chat-Discord-5865F2)](https://discord.gg/bNQudQDKjg)

**A CLI for schema *change***

**retrofit** checks each schema change, advises on its risks, and records it
or stops it. Given any point in that history, it writes the schema; given
two, the migrations between them, forward and reverse.

This repository holds retrofit's binaries and its issue tracker. The demos
at [retrofit.sh](https://retrofit.sh) show retrofit at work.

> **Pre-release.** The SQL that retrofit writes may be wrong, and applying it
> can damage data. Review it before running it against a database you care
> about, and keep backups. Nothing is stable before 1.0.
>
> **Source.** The source is not public yet. The plan is to release it under
> an OSI-approved open-source license before 1.0.

## Install

With [Homebrew](https://brew.sh) on macOS:

```sh
brew install MonotonicHQ/tap/retrofit
```

On Linux or macOS, with the install script:

```sh
curl -fsSL https://retrofit.sh/install | sh
```

The script installs the latest release to `~/.local/bin`, without sudo, and
checks the archive against the release's `checksums.txt` first. Linux needs
glibc 2.34 or later (Ubuntu 22.04, Debian 12, RHEL 9 and newer); macOS needs
13 Ventura or later; both on amd64 or arm64.

The macOS binaries are signed and notarized. Apple is asked to confirm that
on the first run, so that run needs a network connection.

Archives for macOS and Linux are on the
[Releases](https://github.com/MonotonicHQ/retrofit/releases) page.

### Channels

- **Releases** (`retrofit`, versions such as `0.10.0`). A release is a WIP
  build that was chosen and passed the full release checks, rebuilt from the
  same commit. The commands above install the latest.
- **WIP builds** (`retrofit@wip`, versions such as `0.11.0-wip.40`). They are
  published as changes land, once CI passes. The number after `wip` counts
  every build and never resets. Install one to try a fix or a feature before
  it is released, and report issues against the exact version
  (`retrofit --version`).

Before 1.0 neither channel promises compatibility between versions.

### Try a WIP

The two casks conflict, so swap one for the other:

```sh
brew uninstall retrofit
brew install MonotonicHQ/tap/retrofit@wip
```

And back:

```sh
brew uninstall retrofit@wip
brew install MonotonicHQ/tap/retrofit
```

With the install script, pass `--wip` for the newest WIP build, or
`--version` for one release:

```sh
curl -fsSL https://retrofit.sh/install | sh -s -- --wip
curl -fsSL https://retrofit.sh/install | sh -s -- --version 0.10.0
```

## Issues and questions

Report a bug or suggest a change in
[Issues](https://github.com/MonotonicHQ/retrofit/issues/new/choose).
Ask a question or talk with other users on
[Discord](https://discord.gg/bNQudQDKjg).

## License

The binaries are published under the Retrofit Binary License
([LICENSE](LICENSE)), which grants no rights in the source. Every archive
carries the license and its third-party notices. The copyright holders are
listed in [AUTHORS](AUTHORS).
