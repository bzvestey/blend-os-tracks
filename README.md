# Bzvestey's BlendOS track implementation repository

This is the repository is my personal collection of opinionated tracks that I use. This is setup so that I can easily make changes without needing to modify the `/system.yaml` file on each computer, instead I can update the tracks here, and then just run `sudo akshara update` on each computer as needed.

## Available tracks

- `base-headless`: This is the base track that can be used for systems that don't need a graphical interface. Based on [blendos-base](https://github.com/blend-os/tracks/blob/main/blendos-base.yaml) from BlendOS.
- `base-graphical`: This is a common base for graphical tracks to extend with all of the shared tools, like my prefered terminal emulator. This pulls in parts of [gnome](https://github.com/blend-os/tracks/blob/main/gnome.yaml) and [default-gnome](https://github.com/blend-os/tracks/blob/main/default-gnome.yaml) tracks from BlendOS that are not gnome specific.
- `gnome`: This is the gnome desktop manager based track used as by base graphical setup right now, as it is what I know best. This is based on [gnome](https://github.com/blend-os/tracks/blob/main/gnome.yaml) and [default-gnome](https://github.com/blend-os/tracks/blob/main/default-gnome.yaml) tracks from BlendOS.

## Local setup for computer

- Update the `/system.yaml` file and set `impl: https://github.com/bzvestey/blend-os-tracks/raw/main` and then `track: <available track>` to use one of the above tracks.
- If this computer is to use syncthing, then add `  - syncthing@<username>.service` to the `services:` section.
- Run `sudo tailscale set --operator=$USER` to that tailscale can be run at the user level.
- Bring tailscale up `tailscale up` and go through the login steps.
- If the device has a finderprint reader:
    - Run `fprintd-enroll -f right-index-finger` and go through the setup.
    - Run `fprintd-enroll -f left-index-finger` and go through the setup.

## Flatpacks to install

Run `./scripts/flatpaks.sh` to install the flatpaks.


## Imprtant links

- [BlendOS Homepage](https://blendos.co/)
- [BlendOS Repo](https://git.blendos.co/blendOS)
- [BlendOS Packages](https://pkg-repo.blendos.co/)
