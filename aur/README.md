# AUR Package: `hermes-desktop-bin`

This directory contains the AUR template for Arch Linux and its derivatives (Manjaro, EndeavourOS, etc.).

## How it works

1. Whenever a new release is generated on [dalroot/hermes-desktop-linux](https://github.com/dalroot/hermes-desktop-linux/releases), the `.deb` asset checksum is injected into `PKGBUILD`.
2. Arch Linux users can install it directly with any AUR helper:
   ```bash
   yay -S hermes-desktop-bin
   # or
   paru -S hermes-desktop-bin
   ```
