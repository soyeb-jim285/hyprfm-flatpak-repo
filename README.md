# HyprFM Flatpak repository

Self-hosted Flatpak distribution for [HyprFM](https://github.com/soyeb-jim285/hyprfm),
served at <https://hyprfm.soyebjim.me/>.

## Install

HyprFM depends on the KDE Platform runtime from Flathub, so the Flathub remote
must exist at the **same scope** you install into. For a `--user` install, add
both Flathub and HyprFM at user scope before installing:

```
flatpak remote-add --user --if-not-exists \
    flathub https://dl.flathub.org/repo/flathub.flatpakrepo
flatpak remote-add --user --if-not-exists \
    hyprfm https://hyprfm.soyebjim.me/hyprfm.flatpakrepo
flatpak install --user hyprfm io.github.soyeb_jim285.HyprFM
```

If your Flathub remote only exists at system scope, a `--user` install of
HyprFM will fail with an error about `org.kde.Platform` not being installed.
Either add Flathub at user scope as shown above, or drop every `--user` flag
(and prefix the install command with `sudo`) to install system-wide.

After installing, update HyprFM to new releases the same way you would update
any other Flatpak:

```
flatpak update --user io.github.soyeb_jim285.HyprFM
```

## Contents

- `repo/` — ostree repository written by the HyprFM release workflow on each `v*` tag
- `hyprfm.flatpakrepo` — Flatpak remote descriptor (what users point `flatpak remote-add` at)
- `public-key.asc` — GPG public key used to sign the repository; users can verify the key by importing this file

## Source and issues

HyprFM itself is developed at <https://github.com/soyeb-jim285/hyprfm>. File issues there, not here.
