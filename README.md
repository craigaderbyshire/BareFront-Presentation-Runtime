# BareFront Presentation Runtime

Privately installed, patched presentation components for BareFront.

## Release v2

Target platform: Debian 13 (Trixie), amd64.

Components:

- Gamescope 3.16.22
- vkBasalt 0.3.2.10

The patched binaries are installed inside BareFront's
`runtime/presentation/` directory. They do not replace the Debian
system installations.

The installer generates a Vulkan layer manifest containing the
installation-specific absolute path to the private vkBasalt library.

## Changes from v1

BareFront now owns shader selection entirely before emulator launch.

vkBasalt's runtime keyboard shader-toggle handling is disabled, so the
configured `enableOnLaunch` state remains fixed for the emulator session.

The existing BareFront X11 and shutdown fixes are retained.

This keeps emulator controls independent of presentation controls.

## Release assets

- `barefront-presentation-debian13-amd64-v2.tar.xz`
- `barefront-presentation-sources-v2.tar.xz`
- `SHA256SUMS`

The source archive contains the corresponding Debian source packages
and all BareFront patches required to reproduce the modified source.

## Validation status

The published v2 runtime has passed BareFront validation including:

- clean v2 installation
- repeated-install idempotence
- exact v1 to v2 upgrade
- refusal of unknown or modified installed runtimes
- installation-specific Vulkan manifest verification
- BareFront private runtime resolution
- PS1 shader-toggle isolation
- Xbox Guide exit
- Saturn controller disc handling with fixed shader state

The exact public GitHub v2 assets were downloaded through the URL used
by BareFront, their published SHA-256 hashes were verified, and the
binary archive passed isolated fresh-install and reinstall validation.

BareFront verifies the binary archive SHA-256 before installation and
separately checks the installed presentation binaries.
