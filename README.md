# HyprFM Flatpak repository

Self-hosted Flatpak distribution for [HyprFM](https://github.com/soyeb-jim285/hyprfm),
served at <https://hyprfm.soyebjim.me/>.

## Install

```
flatpak remote-add --user --if-not-exists \
    hyprfm https://hyprfm.soyebjim.me/hyprfm.flatpakrepo
flatpak install --user hyprfm io.github.soyeb_jim285.HyprFM
```

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
