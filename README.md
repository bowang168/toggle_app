# toggle_app

A bash utility to toggle terminal application windows on Linux (GNOME). Launches the app if not running, focuses it if running in the background, and minimizes it if already focused.

## Features

- **Launch or focus** any application by its WM_CLASS with a single command
- **Minimize on re-trigger** -- if the target window is already focused, it gets minimized out of the way
- **Automatic retry** -- waits briefly for newly launched applications to register their window
- **Lightweight** -- pure bash with no extra dependencies beyond standard X11 tools

## Requirements

- [xdotool](https://github.com/jordansissel/xdotool)
- [wmctrl](https://sites.google.com/site/aborber/wmctrl)

## Installation

```bash
git clone https://github.com/bowang168/toggle_app.git
cd toggle_app
chmod +x toggle_app
cp toggle_app ~/.local/bin/
```

## Usage

```bash
# Toggle gnome-terminal (default if no argument given)
toggle_app gnome-terminal

# Toggle kitty terminal
toggle_app kitty
```

## Keyboard Shortcut Integration

For the best experience, bind `toggle_app` to keyboard shortcuts in GNOME Settings > Keyboard > Custom Shortcuts. This lets you instantly summon or hide any application with a single key press.

See [OL9 keyboard shortcuts](docs/ol9-shortcuts.md) for my full setup.

## License

MIT
