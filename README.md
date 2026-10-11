# Layla for Linux

An early Linux-native desktop companion prototype. It displays transparent
rendered sprite frames as an always-on-top, draggable desktop character, with
walking and idle animation and a small right-click menu.

This is not yet a port of the Windows companion. It does not include Layla's
chat, voice, screen awareness, music detection, or Windows-specific features.

## Run from source

Requires Python 3.10 or newer and PySide6:

```sh
python3 -m venv .venv
. .venv/bin/activate
python -m pip install --upgrade pip
python -m pip install .
layla-linux --assets /path/to/layla-sprites
```

To start it without arguments, place licensed sprite sequences in
`~/.local/share/layla-linux/assets/`.

The sprite directory must contain complete, consecutively numbered
`idle_000.png` and `walk_000.png` sequences. Use `--help` for the command
options.

For openSUSE Leap, the Python virtual environment can be created with the
system Python package manager's venv support, then PySide6 installed into that
environment with pip. Do not use `sudo pip`.

## Artwork and model rights

The program source is licensed under GNU GPL version 3 or (at your option) any
later version. Character models, textures, and rendered sprite frames are not
included. The upstream model is credited in [ATTRIBUTION.md](ATTRIBUTION.md),
but its exact redistribution terms still need confirmation from its Sketchfab
listing or the model author before any art is published.

## Status

This is a visual proof of concept, not a finished release. The application
currently supports a single primary screen and local sprite files. Linux
desktop integration, packaging, accessibility, and asset licensing need
further work before a public release.
