# BareFront Presentation Runtime v1 — Validation

Target: Debian 13 (Trixie), amd64.

## M7 runtime acceptance

All 16 BareFront systems completed their M7 presentation and
controller-exit acceptance.

Keyboard Esc and Xbox Guide return directly to BareFront.

The release binaries were retained unchanged for distribution.

## Clean Debian installation

A clean Debian 13 XFCE/X11 VM received a source-only BareFront
snapshot. No installed M7 emulators, runtime, ROMs or saves were
transferred.

The BareFront v0.12 installer completed successfully using the
pinned presentation release archive.

Verified:

- Release archive SHA-256.
- Installed Gamescope SHA-256.
- Installed vkBasalt SHA-256.
- VM-specific Vulkan layer manifest.
- No missing linked libraries in the private binaries.
- Installed exit helpers, including Amiberry's SDL2 Guide helper.
- Bash syntax for all 17 production launcher scripts.
- No explicit installer failure markers.

VM gameplay and automatic GitHub-download installation are not
claimed as complete by this validation record.
