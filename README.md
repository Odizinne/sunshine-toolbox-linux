# Sunshine Toolbox for Linux

Sunshine Toolbox is a command-line utility to help automating with Sunshine.

## Requirements

- `gnome-randr` for gnome-wayland resolution manipulation
- `xrandr` for x11 resolution manipulation
- `wmctrl` for `--close-bp` and `--bp-dummy`

## Usage

Available commands:

- `--set-status false/true`: Create / delete `~/.local/share/sunshine_status/status.txt`
- `--close-bp`: Close Steam Big Picture.
- `--bp-dummy`: Start a dummy process that will end as soon as Big Picture is closed.
- `--client-res "ADAPTER" "WIDTH" "HEIGHT" "FPS"`: This command sets the resolution to the client resolution.
- `--default-res "ADAPTER"`: Set `"ADAPTER"` to its default resolution.

## Example

Add as sunshine do_command (replace with your adapter):
```bash
sh -c "sunshine-toolbox --client-res DP-2 ${SUNSHINE_CLIENT_WIDTH} ${SUNSHINE_CLIENT_HEIGHT} ${SUNSHINE_CLIENT_FPS}"
```

Add as sunshine undo_command

```bash
sh -c "sunshine-toolbox --default-res DP-2"
```

`--bp-dummy` allow you to stop a stream by closing Steam Big Picture