# BareFront Presentation Runtime

Privately installed, patched presentation components for BareFront.

## Release v1

Target platform: Debian 13 (Trixie), amd64.

Components:

- Gamescope 3.16.22
- vkBasalt 0.3.2.10

The patched binaries are installed inside BareFront's
`runtime/presentation/` directory. They do not replace the Debian
system installations.

The installer generates a Vulkan layer manifest containing the
installation-specific absolute path to the private vkBasalt library.

## Release assets

- `barefront-presentation-debian13-amd64-v1.tar.xz`
- `barefront-presentation-sources-v1.tar.xz`
- `SHA256SUMS`

The source archive contains the corresponding Debian source packages
and BareFront's three patches.

The repository also contains the patches, release documentation,
and Debian copyright information.

## Validation status

The pinned runtime has passed BareFront's M7 presentation and exit
acceptance across all 16 supported systems.

A clean Debian 13 amd64 XFCE/X11 VM has successfully installed
BareFront from a source-only snapshot using the exact release archive.

Both installed binaries passed SHA-256 verification. The VM-specific
Vulkan manifest, linked-library audit and installer completion checks
also passed.

VM gameplay validation and automatic GitHub-download installation
remain separate acceptance gates.

BareFront verifies the binary archive SHA-256 before installation
and separately checks the two installed binary hashes.
