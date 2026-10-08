# BareFront Presentation Runtime v2 — Validation

Target: Debian 13 (Trixie), amd64.

## Runtime acceptance

The v2 runtime has passed BareFront presentation and controller-exit
acceptance on the BareFront M7.

Validated behaviour includes:

- clean v2 installation
- repeated-install idempotence
- exact known v1 to v2 upgrade
- refusal of unknown or modified installed runtimes
- installation-specific Vulkan layer manifest
- BareFront private runtime resolver
- PS1 gameplay with F8 and Home unable to alter the active shader
- Xbox Guide exit retained
- Saturn controller disc handling retained while shader state remains fixed

## Public release validation

The exact public GitHub v2 assets were downloaded through the release
URL used by BareFront.

Verified:

- Published binary archive SHA-256.
- Published source archive SHA-256.
- Isolated fresh installation from the public binary archive.
- Installation-specific Vulkan manifest.
- Installed presentation runtime verification.
- Repeated installation remains idempotent.

The published v2 source archive contains the corresponding Debian source
packages and all BareFront patches, including the vkBasalt no-toggle
patch introduced for v2.
