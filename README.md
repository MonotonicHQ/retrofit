# retrofit

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

Binaries for macOS and Linux will be published on this repository's
[Releases](https://github.com/MonotonicHQ/retrofit/releases) page.
Install instructions follow the first release.

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
