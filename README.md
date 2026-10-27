# Soravo releases

This repository is artifacts-only. It hosts signed (checksummed) Soravo desktop installers, SHA256SUMS, release notes, and optional minisign signatures.

It does **not** contain source code, secrets, internal documentation, or build logs.

## Verification

Every release contains:

- Installer files named with version and architecture
- SHA256SUMS with bare filenames
- Release notes

Verify a download with:

`
sha256sum -c SHA256SUMS
`

or on Windows:

`
Get-FileHash -Algorithm SHA256 <file>
`

Compare the hash to the published SHA256SUMS.

## Trust

SHA-256 checksums detect accidental corruption and tampering only when compared against a trusted source. Hashes in release notes also protect against some mirror or host corruption.

Self-signed Windows installers may still trigger SmartScreen. This repository intentionally publishes checksums, not publisher claims.
