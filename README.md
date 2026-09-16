# Degen Radio

A focused internet-radio player for the terminal.

Fork of https://github.com/LargeModGames/spotatui.

<img width="1061" height="514" alt="degen-radio" src="https://github.com/user-attachments/assets/7bdb4442-1df2-4b1f-b5b5-b8f7f57d0fbb" />


Search the [Radio Browser](https://www.radio-browser.info/) directory, save favorite stations, stream them through your system audio output, and see live song metadata. No account or subscription required.

## Install

```bash
git clone https://github.com/ethereumdegen/degen-radio.git
cd degen-radio
cargo install --path . --locked
degen-radio
```

Degen Radio currently targets Linux and integrates with MPRIS for desktop media controls.

## Controls

| Key | Action |
|---|---|
| `s` or `/` | Search for stations |
| Arrow keys or `h`/`j`/`k`/`l` | Move between panels and stations |
| `Enter` | Play the selected station |
| `f` | Add a favorite |
| `d` or `D` | Remove a favorite |
| `Space` | Pause or resume |
| `+` / `-` | Change volume |
| `x` | Open or close settings |
| `X` | Stop playback |
| `q` | Quit |

The search box, station panels, and settings also support mouse input.

## Themes

Open settings with `x`, choose a preset with `Up`/`Down`, and apply it with `Enter`.

Included presets: Tokyo Night, Catppuccin, Osaka Jade, Gruvbox, Nord, and Rose Pine.

## Omarchy tray plugin

The companion [Degen Radio for Omarchy](https://github.com/ethereumdegen/omarchy-degen-radio-plugin) plugin adds a tray widget with now-playing metadata, playback controls, and saved-station switching.

```bash
omarchy plugin add https://github.com/ethereumdegen/omarchy-degen-radio-plugin.git --enable
```

## Data

Favorites and settings are stored in `$XDG_STATE_HOME/degen-radio/state.yml`. Existing Spotatui radio favorites are imported automatically from `~/.local/state/spotatui/state.yml` when no Degen Radio state exists.

## External control

```bash
# List saved stations
degen-radio radio list --json

# Switch the running player to a stream
degen-radio radio play https://ice1.somafm.com/groovesalad-128-mp3
```

## Development

```bash
cargo run
cargo test --locked
```

Degen Radio is derived from [Spotatui](https://github.com/LargeModGames/spotatui) and is available under the MIT license.
