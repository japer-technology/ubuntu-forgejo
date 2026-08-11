# Release

Product versions use `yyyy.mm.dd.hh.nn.ss` UTC format. The standalone
`forgejo-<VERSION>.tar.gz` source artifact contains the application tree at
its root, the family schemas, and the repository license.

The pinned
[upstream release workflow](https://github.com/japer-technology/ubuntu-zombie/blob/main/.github/workflows/forgejo-release.yml)
runs lint, unit, integration, and schema checks; packages the source;
creates test evidence and an SPDX SBOM; computes checksums; attests provenance; signs every asset with keyless
cosign; and publishes tag `forgejo-v<VERSION>`.

This source release does not redistribute the upstream Forgejo binary. The
lifecycle retrieves and verifies the selected official binary during install
or update.
