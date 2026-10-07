# UrukOS Brand Guide

## Name and tagline

- Product name: **UrukOS** (never "Fedora" in branding).
- Tagline: "The fire of Uruk, on your desktop."
- Based on Fedora Linux: UrukOS is an independent project, not affiliated with or endorsed by the Fedora Project or Red Hat.

## Palette (single source of truth: `brand/palette.json`)

| Token | Name | Hex | RGB | Use |
|---|---|---|---|---|
| bg | Sumerian Night | `#0A0A0C` | 10,10,12 | primary background |
| surface | Ziggurat Stone | `#1C1917` | 28,25,23 | terminal bg, panels, cards |
| accent | Uruk Amber | `#FF8C00` | 255,140,0 | active, selected, progress |
| accent2 | Gilgamesh Bronze | `#A65D24` | 166,93,36 | borders, secondary buttons |
| fg | Clay Tablet | `#FCF3E5` | 252,243,229 | text |

Rules: Bronze is borders/icons only (~3.5:1 contrast), never body text. Store hex values only in `palette.json`; regenerate everything with `tools/gen-palette.py`.

## Logo

- `brand/logo.svg` — primary (amber on Sumerian Night).
- `brand/logo-mono.svg` — monochrome variant for dark surfaces.
- `brand/favicon.svg` — small-size variant.
- `brand/wordmark.svg` — text lockup.

Minimum clear space: half the height of the gate mark on all sides. No recoloring, stretching, drop shadows, or rotation.

## Wallpapers

- `wallpapers/urukos-ziggurat.svg` + exported 3840x2160 / 1920x1080.
- `wallpapers/urukos-night.svg` + exported 3840x2160 / 1920x1080.

## KDE

- Color scheme: `kde/colors/UrukOS.colors` (generated).
- Look-and-feel package: `kde/look-and-feel/org.urukos.desktop/`.
- Avatar: `kde/avatar/urukos-avatar.png`.
- Wallpaper: use `wallpapers/urukos-ziggurat-3840x2160.png`.

Login screen: Fedora 44 uses Plasma Login Manager, which does not support arbitrary QML themes. Brand it via wallpaper and Plasma settings only.

## Terminal

- Ghostty: `terminal/ghostty/urukos`
- fish: `terminal/fish/urukos.theme`
- tmux: `terminal/tmux/urukos.conf`
- bat: `terminal/bat/themes/urukos.tmTheme`
- eza: `terminal/eza/theme.yml`
- fastfetch: `terminal/fastfetch/config.jsonc` (place `fastfetch-logo.txt` at `/usr/share/urukos/fastfetch-logo.txt`)

All generated. Do not hand-edit.

## Plymouth

`plymouth/urukos/` — `urukos.plymouth` + `urukos.script` (generated colors) + `images/watermark.png`.

## Contrast

Run `python3 tools/contrast-report.py`; see `docs/contrast-report.md`.
