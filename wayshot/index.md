---
layout: layout.njk
title: Wayshot
---

<p align=center>
  <img src="{{ '/assets/img/wayshot.png' | url }}" alt=wayshot width=60%>
  <p align=center>A native screenshot tool for wlroots based compositors such as
  sway and river written in Rust. X11 support coming soon. <a href="https://git.sr.ht/~shinyzenith/wayshot">sourcehut</a></p>
  
  <p align="center">
  <img src="https://img.shields.io/github/license/waycrate/wayshot?style=flat-square&logo=appveyor">
  <img src="https://img.shields.io/badge/cargo-v1.1.2-green?style=flat-square&logo=appveyor">
  <img src="https://img.shields.io/github/issues/waycrate/wayshot?style=flat-square&logo=appveyor">
  <img src="https://img.shields.io/github/forks/waycrate/wayshot?style=flat-square&logo=appveyor">
  <img src="https://img.shields.io/github/stars/waycrate/wayshot?style=flat-square&logo=appveyor">
  </p>
</p>

# Usage:

Region Selection:

```bash
wayshot -s "$(slurp -f '%x %y %w %h')"
```

Fullscreen:

```bash
wayshot
```

Custom file path:

```bash
wayshot -f ../screenshot.png --extension jpg
```

Screenshot and copy to clipboard:

```bash
wayshot --stdout | wl-copy
```

Pick a hex color code, using ImageMagick:

```bash
wayshot -s "$(slurp -p -f '%x %y %w %h')" --stdout | convert - -format '%[pixel:p{0,0}]' txt:-|egrep "#([A-Fa-f0-9]{6}|[A-Fa-f0-9]{3})" -o
```

Pick a color, using ImageMagick:

```bash
wayshot -s "$(slurp -p -f '%x %y %w %h')" --stdout | convert - -format '%[pixel:p{0,0}]' txt:-
```
# Installation

## AUR:
`wayshot-git` & `wayshot-bin` have been packaged.

## Compile time dependencies:
-   rustup
-   make

## Compiling:
-   `git clone https://github.com/waycrate/wayshot && cd wayshot`
-   `make setup`
-   `make`
-   `sudo make install`

# Support:

1 - Use the mailing list.

2 - You can also join us on Matrix at ([#wayshot:matrix.org](https://matrix.to/#/#wayshot:matrix.org)), which is also bridged to our [Discord server](https://discord.gg/KKZRDYrRYW), depending on which you prefer.


# Smithay Developers:

Massive thanks to smithay developer <a href="https://github.com/cmeissl">Cmeissl</a> and <a href="https://github.com/vberger">Victor Berger</a>. Without them this project won't be possible as my wayland knowledge is limited.
