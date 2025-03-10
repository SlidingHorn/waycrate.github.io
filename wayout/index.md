---
layout: layout.njk
title: Wayout
---
<p align=center>
  <img src="{{ '/assets/img/wayout.png' | url }}" alt=wayout width=60%>
  <p align=center>A simple output management tool for wlroots based compositors
  implementing zwlr_output_power_management_v1. <a href="https://git.sr.ht/~shinyzenith/wayout">sourcehut</a></p>
  
  <p align="center">
  <img src="https://img.shields.io/github/license/waycrate/wayout?style=flat-square&logo=appveyor">
  <img src="https://img.shields.io/badge/cargo-v1.0.0-green?style=flat-square&logo=appveyor">
  <img src="https://img.shields.io/github/issues/waycrate/wayout?style=flat-square&logo=appveyor">
  <img src="https://img.shields.io/github/forks/waycrate/wayout?style=flat-square&logo=appveyor">
  <img src="https://img.shields.io/github/stars/waycrate/wayout?style=flat-square&logo=appveyor">
  </p>
</p>

# Usage:
List output states:
```bash
wayout
```

Turn on a display:
```bash
wayout --on <your output name>
```

Turn off a display:
```bash
wayout --off <your output name>
```

Toggle the state of a display:
```bash
wayout --toggle <your output name>
```
# Installation

## AUR:
`wayout-git` has been packaged.

## Compile time dependencies:
-   rustup
-   make

## Compiling:
-   `git clone https://github.com/waycrate/wayout && cd wayout`
-   `make setup`
-   `make`
-   `sudo make install`

# Support:

1 - Use the mailing list.

2 - You can also join us on Matrix at ([#wayout:matrix.org](https://matrix.to/#/#wayout:matrix.org)), which is also bridged to our [Discord server](https://discord.gg/KKZRDYrRYW), depending on which you prefer.
