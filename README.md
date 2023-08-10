# Waypaper

GUI wallpaper setter for both Wayland and X11 window managers that works as a frontend for popular backends like `swaybg`, `swww`, and `feh`.

![screenshot](screenshot.jpg)

## Features

- Support for GIF animations (with `swww` backend)
- GUI wallpaper selection
- Works on both Wayland and X11
- Restores wallpaper on launch of your WM with `waypaper --restore`
  
## Installation

1) Install a preferred backend from your package manager: [swaybg](https://github.com/swaywm/swaybg) or [swww](https://github.com/Horus645/swww) on Wayland or [feh](https://github.com/derf/feh) on x11.
2) Install waypaper as: `pipx install waypaper`

If `pipx` is not found, you first need to install `pipx` from your package manager, it's sometimes called `python-pipx`.

### AUR package

[waypaper-git](https://aur.archlinux.org/packages/waypaper-git) package is available in AUR. So, if you are on arch-based system, you can install it as `yay -S waypaper-git`.

### Dependencies

- `swaybg` or `swww`
- gobject python library (it might be called `python-gobject` or `python3-gi` or `python3-gobject` in your package manager.)

## Usage

`waypaper` command will run GUI application.

To restore the chosen wallpaper at launch, add `waypaper --restore` to your startup config. For example:

*In Hyprland*

`exec-once=waypaper --restore`

*In Sway or I3*

`exec waypaper --restore`

## Backends

- [swaybg](https://github.com/swaywm/swaybg) - the wayland backend that supports only static images.
- [swww](https://github.com/Horus645/swww) - the wayland backend that supports animated GIFs.
- [feh](https://github.com/derf/feh) - the x11 backend that supports static images.

## Troubleshooting

- If wallpaper does not change, make sure that `swaybg` or `swww` is installed.
- If application does not run, make sure to install gobject library (it might be called `python-gobject` or `python3-gi` in your package manager). Although it is supposed to be installed automatically with the package.
- Please understand that not all backends work on all system, choose the right one for your can and stick to it.

## Roadmap

- Support for other backends like ~swww~, ~feh~, and hyprpaper.
- Additional options for ~search in subfolders~, background colors etc.
- Dynamic grid of thumbnails that adopts to the application width.
- Improve loading of folders with many images.

## Contributions

Feel free to propose PR and suggest the improvements.
If you'd like to support the development, consider [donations](https://www.buymeacoffee.com/angryprofessor).
