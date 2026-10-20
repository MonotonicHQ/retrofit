# Security policy

## Reporting a vulnerability

Report a vulnerability privately, through
[GitHub's private vulnerability reporting](https://github.com/MonotonicHQ/retrofit/security/advisories/new).
Do not open a public issue or post it on Discord.

Include:

- the version (`retrofit --version`), the platform, and how retrofit was
  installed;
- the steps, and the input (SQL, oplog or config), that reproduce it;
- what an attacker could do with it.

You will get a timely response. The report stays private between you and
the maintainers until a fix is released and the advisory is published.
Unless you ask otherwise, the advisory credits you.

## What to report here

Report privately anything that lets input, or a release, do more than it
should. For example:

- input that makes retrofit run code, or read or write files outside the
  project;
- a flaw in the install script, the checksums, or the signing of the
  release archives.

No retrofit command connects to a database, so the SQL it writes runs only
when you apply it. Before 1.0, review all of it before applying it, and edit
it where it is wrong. A fault in that SQL, such as a migration that fails,
drops something it should not, or quotes a name wrongly, is a bug. Report it
in [Issues](https://github.com/MonotonicHQ/retrofit/issues/new/choose).

## Supported versions

Before 1.0, fixes land in a WIP build first and then in the next release.
Earlier releases are not patched; upgrade to get a fix.
