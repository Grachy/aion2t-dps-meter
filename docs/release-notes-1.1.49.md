# Release 1.1.49

## Boss respawns and overlays

- Hide the boss respawn overlay when the game is minimized, absent or another application is active. Restore it passively when the game returns; retain its open state and saved preferences.
- In Alerts, show the character's home region first: Altgard for Asmodians, Verteron for Elyos. Determine faction from the confirmed home server, independent of the current map or interface language. Preserve the countdown order within each region.
- Refresh ordering after character changes even when the timers have not changed. An unknown faction retains the current-location fallback.
- Show a visible unlock hint for locked overlay windows using the configured shared shortcut and Alt+click. Existing lock and opacity controls remain available.

## Replays and dungeon gathering

- Correct read-only replay damage attribution for known effects and explicit summon ownership. Let the viewer include or exclude eligible nonboss adds, and persist that choice.
- Recorded regression checks align six original replays and thirty participant totals with fight history when adds are included. Original recordings and stored damage amounts are unchanged.
- Restore validated cross-server members in dungeon gathering when their encoded member keys differ from their home servers. Preserve empty party slots.

## Validation and remaining checks

- Optimized native x64 build and NSIS packaging succeeded. The full browser UI/tools suite passed with 28 obfuscated modules and all 17 boss overlay scenarios. Verified 1,735 source inputs, 1,286 final assets and native/installer version metadata.
- Retain the latest cargo check, 55 passing focused Rust tests, and previous recorded replay/party-room checks; these were not repeated solely for packaging.
- Capture party-room parsing and combat replay projection changed since 1.1.48. Fresh in-game minimize/restore, Alt+Tab, lock/shortcut and cross-server join/leave/ready checks remain before wider distribution, together with the existing live combat checks.
- Other players' full ordinary damage at public bosses remains unresolved, including party/raid members.

Includes previous 1.1.48 replay, checklist, resource-map, fight-detail and installer improvements.

Installer: [aion2t-dps-setup-1.1.49-x64.exe](aion2t-dps-setup-1.1.49-x64.exe) (31,064,144 bytes).

SHA-256: `3e3115da3902078239d72055c9ce161c612744527890772dc7b16bb3ba05a17c`.
