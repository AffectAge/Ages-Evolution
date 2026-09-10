# FancyMenu configuration

This directory is the **source-of-truth** for the FancyMenu files shipped by Ages Evolution.

## Install

Copy this directory to the Minecraft instance's `config/` directory:

```text
src/config/fancymenu/customization/title_screen_layout.txt
src/config/fancymenu/assets/ages-evolution-feed.md
```

becomes:

```text
.minecraft/config/fancymenu/customization/title_screen_layout.txt
.minecraft/config/fancymenu/assets/ages-evolution-feed.md
```

Then open the FancyMenu customization screen and reload FancyMenu.

## GitHub release panel

The title-screen layout fetches the live Markdown feed from:

```text
https://raw.githubusercontent.com/AffectAge/Ages-Evolution/main/src/config/fancymenu/assets/ages-evolution-feed.md
```

The feed is updated by `.github/workflows/update-fancymenu-feed.yml` whenever a GitHub Release is published.

This means the main menu can show a new version and release notes without requiring a new FancyMenu layout file.

## Required mods

The layout targets FancyMenu 3.x on Minecraft 1.21.1. The current FancyMenu project provides NeoForge builds for 1.21.1.

The `MODS` button uses the ModMenu widget identifier. If ModMenu is not installed in a particular instance, remove that custom button or replace its action with the mod-list screen supplied by the installed menu mod.

## Planned assets

The layout intentionally does not require custom PNG/OGG assets yet. The next UI pass can add:

- custom sci-fi button normal/hover textures;
- logo artwork;
- scanline / HUD overlays;
- hover and click sounds;
- looping menu music;
- animated background/video/shader;
- dedicated changelog screen.
