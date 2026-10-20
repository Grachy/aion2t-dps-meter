# Release 1.1.48

## Combat replays

- Show the boss on the map with a separate target card, HP/stagger tracks and one horizontal row of effects. Boss events appear below the map.
- Use compact party cards so the group fits better. Each player's effects show one row by default and can be expanded. Redundant coordinates below names are removed.
- Include original client icons, boss portraits and supported attack areas, plus recorded target and gauge events.

## Overlay windows

- Boss respawns and dungeon group windows now have a background-opacity icon (0–100%) and click-through lock button. Text and icons retain their opacity.
- Ctrl+M, or the saved custom binding, controls visible mini-map, mini checklist, activity timers, boss respawns and dungeon group windows together. Alt+click unlocks one window and consumes the complete gesture.
- Full-checklist opacity/lock controls are removed; its settings button is beside Close. Mini-checklist controls remain available.
- Retain legacy transparent boss backgrounds and independent saved opacity settings. Compact checklist settings open in a separate sidebar.

## Checklist, details and maps

- Mark weekly base limits complete even when bonus entries remain, including Daily Dungeon and Ascension Trial.
- Update shop/morph data and use client terminology and translated interface labels in ten languages.
- Improve fight-detail layout and readability, repair detached-window dragging, and retain each participant's class icon in history, including repeated classes.
- Use verified client resource-map candidates and item icons. Candidate locations do not mean all nodes spawn simultaneously.

## Installation and validation

- Interactive setup recommends Borderless Window or Window mode because Fullscreen does not display the overlay. Silent updates skip this message; Npcap prerequisite checks remain.
- Optimized x64 native build and NSIS packaging succeeded. The final build passed the full browser suite with 28 obfuscated modules; 1,725 source files, 1,286 final assets and version metadata were verified.
- Prior native/recorded checks are retained, including forty isolated Alt-click cycles and all four tool-window slots. They were not rerun solely for packaging.
- Replay capture/combat collection changed; verify boss targets, stagger, effects and attack areas against fresh live capture before wider distribution. Physical Ctrl+M/Alt+click and the interactive installer notice also need in-game/interactive checks.
- Other players' full ordinary damage at public bosses remains unresolved, including party/raid members.

Includes previous 1.1.47 party-damage and Alt+click fixes.

Installer: [aion2t-dps-setup-1.1.48-x64.exe](aion2t-dps-setup-1.1.48-x64.exe) (31,060,541 bytes).

SHA-256: `a2559224c0b39f0abed5454cc232780f920ad952861bd3d162315768d5f0d48e`.
