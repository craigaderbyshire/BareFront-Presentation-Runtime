BareFront Presentation Runtime v2
Target: Debian 13 (Trixie), amd64

Contents:
  runtime/gamescope/gamescope
  runtime/vkbasalt/libvkbasalt.so

These are BareFront's privately patched presentation components.
They do not replace the Debian system installations.

The installer creates vkBasalt.json with an absolute library_path
pointing to this installation's runtime/vkbasalt/libvkbasalt.so.

The archive intentionally does not include a machine-specific manifest.

Compared with v1, v2 also disables vkBasalt's runtime keyboard
shader-toggle path. BareFront owns shader selection before emulator
launch, and the configured enableOnLaunch state remains fixed for
the emulator session.

Original Debian source packages and BareFront modifications are supplied
in the accompanying v2 source archive.
