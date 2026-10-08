BareFront Presentation Runtime v2 — corresponding source

Gamescope:
  Debian source version: 3.16.22+ds-1~bpo13+1

Apply patches in this order:
  gamescope-3.16.22-sdl-shutdown.patch
  gamescope-3.16.22-vblank-shutdown.patch

vkBasalt:
  Debian source version: 0.3.2.10-1

Apply patches in this order:
  vkbasalt-0.3.2.10-x11-shutdown.patch
  vkbasalt-0.3.2.10-barefront-no-toggle.patch

The X11 shutdown patch avoids closing the X11 display during
process teardown.

The BareFront no-toggle patch removes vkBasalt's runtime keyboard
shader-toggle path. BareFront selects the shader before emulator
launch, and the configured enableOnLaunch state remains fixed for
the emulator session.

The original Debian .dsc files and source archives are included
in the published v2 source archive.

The patches document BareFront's modifications.
