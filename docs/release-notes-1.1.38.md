# Release 1.1.38

## Bug fixes

- Restored normal clicks and dragging for the unlocked DPS Meter, Combat Assist and notification overlays. Alt is no longer required to move unlocked panels.
- Click-through now follows the explicit **Lock position** setting. Locked and empty panels continue to pass clicks to the game.
- Fixed placement panels disappearing when focus moved to the meter settings.
- Unlocked panels show named frames for placement, even without active cooldowns or notifications. Combat Assist and notification locks remain independent.
- Panels stay within the visible game window and hide when the game is minimized or an unrelated application is active.

Includes the features and fixes from 1.1.37.

## Known limitation

Global ping can remain unavailable when installed Npcap does not support the requested
synchronized clock mode. The proposed compatibility fallback is not included in this
release. Npcap installation and driver updates are unchanged.

Validation: Rust checks, two mouse/visibility regressions and the built frontend browser
checks passed, including unlocked dragging without Alt and locked drag prevention.
Live placement in the game still needs confirmation.

Installer: `aion2t-dps-setup-1.1.38-x64.exe` (15559188 bytes).
SHA-256: `1ad4ffd5469f84ab26381cb44476a78644388ea57db2c46dbe02729af143ddfe`.
