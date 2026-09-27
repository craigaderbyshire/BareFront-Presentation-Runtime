BareFront Presentation Runtime v1 — release candidate
Target: Debian 13 (Trixie), amd64

Contents:
  runtime/gamescope/gamescope
  runtime/vkbasalt/libvkbasalt.so

These are BareFront's privately patched presentation components.
They do not replace the Debian system installations.

The installer must create vkBasalt.json with an absolute library_path
pointing to this installation's runtime/vkbasalt/libvkbasalt.so.

The archive intentionally does not include a machine-specific manifest.

Original Debian source packages and BareFront modifications are supplied
in the accompanying sources archive.

This candidate must pass clean-VM validation before public release.
