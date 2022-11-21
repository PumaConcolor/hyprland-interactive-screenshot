# hyprland-interactive-screenshot

hyprland-interactive-screenshot is a simple bash script to take screenshot easly on Hyprland. It is a fork of [sway-interactive-screenshot](https://github.com/moverest/sway-interactive-screenshot). Just launch the script and it will ask you what you want to take a screenshot.


## Dependencies

- `hyprland` obviously
- `jq` to parse `swaymsg` JSON response that lists windows
- `tofi` to prompt what you want to take a screenshot of
- `grim` to take the screenshot
- `slurp` to select an area on the screen
- [`swappy`](https://github.com/jtheoof/swappy) (optional) to edit the captured screenshot
- `wl-copy` to copy the screenshot to the clipboard

## Bind it to the `Print` key

To bind this script to the `Print` key, just add this to your `~/.config/hypr/hyprland.conf`:

```
bind=,PRINT,exec,/path/to/hyprland-interactive-screenshot
```

## Settings

You can change the directory where screenshots are saved by setting the `HYPRLAND_INTERACTIVE_SCREENSHOT_SAVEDIR` environment variable to another directory.
