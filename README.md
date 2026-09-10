# Ages Evolution — FancyMenu UI

Configuration source for the **Ages Evolution** Minecraft modpack menu.

## Source layout

`src/config/` mirrors the files that should be copied into the Minecraft instance `config/` directory.

```text
src/config/
└── fancymenu/
    ├── customization/
    │   └── title_screen_layout.txt
    └── assets/
        └── ages-evolution-feed.md
```

## Current target

- Minecraft 1.21.1
- NeoForge
- FancyMenu 3.x
- Dark sci-fi / industrial presentation
- Main buttons positioned on the left
- Update / changelog information on the right
- Version and system status in the lower area

FancyMenu's current documentation supports web text sources and JSON/web placeholders, so the update panel is designed around a remote GitHub-hosted Markdown feed rather than hard-coding release notes into the layout.

## Installation

Copy the contents of `src/config/` into the modpack's `config/` directory. The resulting path must be:

```text
config/fancymenu/customization/title_screen_layout.txt
config/fancymenu/assets/ages-evolution-feed.md
```

Open FancyMenu's customization menu and reload FancyMenu after installing or changing the layout.

## GitHub update feed

The menu reads the feed from this repository. A GitHub Actions workflow will update the feed whenever a release is published.

The feed is deliberately plain Markdown so FancyMenu's Text element can render it directly and the menu remains functional even if the GitHub API format changes.
