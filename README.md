# UrukOS-assets

Brand system for UrukOS: logos, wallpapers, Plymouth theme, KDE assets and terminal themes, all generated from a single palette definition.

## How it fits

Part of the UrukOS project:

- [UrukOS-assets](https://github.com/j0yb0y-m/UrukOS-assets) — this repo (branding source)
- [UrukOS-repo](https://github.com/j0yb0y-m/UrukOS-repo) — RPM specs/COPR that package these assets
- [UrukOS-distro](https://github.com/j0yb0y-m/UrukOS-distro) — KIWI build files that install the packages into the ISO

Data flow: **assets** (source art/themes) → packaged as RPMs by **repo** → installed into the ISO by **distro**.

## Quick start

```bash
python3 tools/gen-palette.py          # regenerate all theme files from brand/palette.json
python3 tools/gen-palette.py --check  # verify generated files are in sync
python3 tools/contrast-report.py      # regenerate the palette contrast report
```

## Directory map

```
brand/            logo (primary, mono, favicon SVG), wordmark, palette.json, brand-guide.md
wallpapers/       SVG sources + exported 3840x2160 and 1920x1080
plymouth/urukos/  urukos.plymouth, urukos.script, images/
kde/              look-and-feel, color scheme (UrukOS.colors), login wallpaper, avatar
terminal/         ghostty theme, fish theme, tmux colors, bat/eza themes, fastfetch config + logo
fonts/FONTS.md    list of font PACKAGES to install. NO font binaries in this repo.
tools/            gen-palette.py (+ --check mode), contrast-report.py
docs/             STATUS.md, THIRD_PARTY.md
```

## Contributing

See the UrukOS agent guide in the parent folder. Conventional Commits, English docs, palette changes go through `brand/palette.json` + `tools/gen-palette.py` — never hand-edit generated theme files.

## License

MIT. Copyright (c) 2026 Mahdi (J0yB0y). See [LICENSE](LICENSE). Third-party art/fonts keep their own licenses (see `docs/THIRD_PARTY.md` when present).