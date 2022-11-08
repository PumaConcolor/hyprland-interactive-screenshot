# hyprland-interactive-screenshot

hyprland-interactive-screenshot is a simple bash script to take screenshot easly on Hyprland. It is a fork of sway-interactive-screenshot. Just launch the script and it will ask you what you want to take a screenshot.

## Install

If you are using Archlinux, you can install hyprland-interactive-screenshot with the AUR package [`hyprland-interactive-screenshot`](https://aur.archlinux.org/packages/hyprland-interactive-screenshot) (e.g. `yay -S hyprland-interactive-screenshot`).

## Dependencies

- `hyprland` obviously
- `jq` to parse `swaymsg` JSON response that lists windows
- `rofi` to prompt what you want to take a screenshot of
- `grim` to take the screenshot
- `slurp` to select an area on the screen
- [`swappy`](https://github.com/jtheoof/swappy) (optional) to edit the captured screenshot
- `notify-send` to send a notification to notification daomon (such as [`mako`](https://github.com/emersion/mako))
- `wl-copy` to copy the screenshot to the clipboard

## Bind it to the `Print` key

To bind this script to the `Print` key, just add this to your `~/.config/hypr/hyprland.conf`:

```
bind=,PRINT,exec,/path/to/hyprland-interactive-screenshot
```

## Settings

By default, `hyprland-interactive-screenshot` saves the screenshots in the home directory. You can change that by setting the `HYPRLAND_INTERACTIVE_SCREENSHOT_SAVEDIR` environment variable to another directory.
