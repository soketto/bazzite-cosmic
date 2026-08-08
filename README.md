# Bazzite COSMIC &nbsp; [![bluebuild build badge](https://github.com/soketto/bazzite-cosmic/actions/workflows/build.yml/badge.svg)](https://github.com/soketto/bazzite-cosmic/actions/workflows/build.yml)

Custom image built from Bazzite GNOME images, adding COSMIC DE from the [COPR](https://copr.fedorainfracloud.org/coprs/ryanabx/cosmic-epoch/), COSMIC apps, and some small tweaks. As the COSMIC DE is still in alpha, be aware that there are still constant bugs and missing features (e.g. night light).

Forked from [koitorin/bazzite-cosmic](https://github.com/koitorin/bazzite-cosmic), trimmed down and personalised to my own taste.

### List of tweaks
- Added Fcitx5 as workaround for Japanese input. ([Issue upstream](https://github.com/pop-os/cosmic-epoch/issues/104))
- Added [adicional COSMIC applets](https://copr.fedorainfracloud.org/coprs/wiiznokes/cosmic-applets-unofficial/).
- Added [COSMIC flatpak repo](https://github.com/pop-os/cosmic-flatpak) by default, for apps that are not suitable for Flathub.
- Added **opensnitch** + opensnitch-ui application firewall.

## Rebase

### AMD/Intel
```bash
rpm-ostree rebase ostree-unverified-registry:ghcr.io/soketto/bazzite-cosmic:latest
```

### Nvidia Turing or later
```bash
rpm-ostree rebase ostree-unverified-registry:ghcr.io/soketto/bazzite-cosmic-nvidia-open:latest
```

### Rebase to the signed image
```bash
rpm-ostree rebase ostree-image-signed:docker://ghcr.io/soketto/bazzite-cosmic:latest
rpm-ostree rebase ostree-image-signed:docker://ghcr.io/soketto/bazzite-cosmic-nvidia-open:latest
```
