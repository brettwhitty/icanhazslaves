# `./private`

## Purpose

This directory is intended as a private workspace for sensitive artifacts
that are in the process of being incorporated into the public-facing
repository, or other types of content related to custom usage or testing.

## Encryption

`git-crypt` is used for encryption.

### Configuration

`.gitattributes` in the repo root is used to configure `git-crypt`.

---
**NOTE**
By default, all contents of `./private` are unencrypted.

Newly added directories must be configured in `.gitattributes`:

`...`
`private/docs/** filter=git-crypt diff=git-crypt`
`private/<MY_NEW_SUBDIR>/** filter=git-crypt diff=git-crypt`
`...`
---
