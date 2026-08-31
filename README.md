# Solarized Light for Omarchy

A [Solarized Light](https://ethanschoonover.com/solarized/) theme for
[Omarchy](https://omarchy.org/), built on the canonical 16-color Solarized
palette (eight monotones, eight accents) by Ethan Schoonover.

Companion theme: [omarchy-solarized-dark](https://github.com/chadhs/omarchy-solarized-dark)
— the two share accent values and mirrored monotone assignments, so switching
between them keeps the same feel, per Solarized's dual-mode design.

## Install

```bash
omarchy theme install https://github.com/chadhs/omarchy-solarized-light.git
```

Or clone it wherever you like and copy/symlink it to
`~/.config/omarchy/themes/solarized-light/`, then:

```bash
omarchy theme set solarized-light
```

## Palette

| Solarized | Hex       | Omarchy role |
|-----------|-----------|--------------|
| base3     | `#fdf6e3` | `background`, terminal color 15 |
| base2     | `#eee8d5` | `selection`, `lighter_background`, `hyprland_inactive_border` |
| base1     | `#93a1a1` | `muted` (comments, disabled text, bright black) |
| base0     | `#839496` | `dark_foreground` |
| base00    | `#657b83` | `foreground` (body text, cursor) |
| base01    | `#586e75` | `light_foreground`, `bright_foreground` |
| yellow    | `#b58900` | `yellow` |
| orange    | `#cb4b16` | `orange` |
| red       | `#dc322f` | `red` |
| magenta   | `#d33682` | `magenta` |
| violet    | `#6c71c4` | `brown` (8th accent slot) |
| blue      | `#268bd2` | `accent`, `blue` |
| cyan      | `#2aa198` | `cyan`, second active-border gradient stop |
| green     | `#859900` | `green` |

### Design notes

- Text pairing follows Schoonover's own reading pairs, inverted for light
  mode: `base3:base00` for body text on the plain background and
  `base2:base01` for text on highlighted surfaces (selection, raised panels,
  cursorline). The L\*a\*b lightness difference between the two pairs is
  identical to the dark mode's, by design.
- `dark_background` (`#f9f2e0`) and `darker_background` (`#f2ecd8`) are base3
  stepped toward base2, keeping the warm cream hue instead of graying out;
  `lighter_background` is base2, the canonical highlighted-surface tone.
- The Hyprland active border is a blue→cyan gradient (`#268bd2 #2aa198
  45deg`) over the base3 background; the inactive border is base2.
- Accents are kept identical between the light and dark themes, matching
  Solarized's terminal palettes, so syntax colors don't shift between modes.

## Backgrounds

Three generated, palette-only wallpapers in `backgrounds/`:

1. `1-ridge.png` — calm low-poly landscape (default): a single faceted sky
   over three gently rolling ridges, a round yellow sun, and hairlines along
   the ridges sweeping through all eight Solarized accents — red, orange,
   yellow, green, and cyan on the far ridge; blue, violet, and magenta on
   the mid ridge. This is also the wallpaper used for the theme previews.
2. `2-daybreak.png` — diagonal base3→base2 fade
3. `3-glow-blue.jpg` — radial blue glow on base3
4. `4-glow-sun.jpg` — radial warm yellow glow on base3

Cycle with `omarchy theme bg next`, or add your own to
`~/.config/omarchy/backgrounds/solarized-light/`.

## Scope

`colors.toml` is the source of truth: Omarchy generates the terminal configs
(Alacritty, Foot, Kitty, Ghostty), Hyprland border colors, Neovim, btop,
VS Code, and shell/bar theming from it at `omarchy theme set` time. This repo
ships only palette-derived color data and imagery.

## Credits

- [Solarized](https://ethanschoonover.com/solarized/) palette by Ethan
  Schoonover (MIT).
- Role mapping informed by the same reading-pair approach used in the
  [Solarized theme for T3 Code](https://github.com/chadhs/dotfiles/tree/master/utils/t3-code/themes/solarized).
