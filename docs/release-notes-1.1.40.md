# Release 1.1.40

## New and improved

- Reorganized Settings into eight clear sections with a fixed sidebar. Controls, integrations, and diagnostics now have their own sections. Old small saved window sizes expand so all tabs stay accessible. The original dark gray and green colors and square corners are preserved.
- Added a Combat Assist boss-skill display choice: show both casts and cooldowns, casts only, or cooldowns only. The existing cast sound alerts still work when only cooldowns are shown.
- A locked meter now keeps the unlock instructions visible next to the padlock. It shows Alt+click and the current hotkey (Ctrl+L by default). Fixed Alt+click unlocking the meter. The meter resize grip is smaller and frameless.

- Added one-click in-app updates. When a newer release has a verified installer, the Update button downloads it, checks its SHA-256, starts a silent installation, and closes the meter. Windows may request administrator approval.

## Combat accuracy fixes

- Improved party tracking when multiple players share a class, including Spiritmasters and their summons. Damage rows are no longer merged solely because class names match.
- Isolated personal buff ownership so another character of the same class cannot make your Combat Assist show a buff you do not have.
- Corrected Insignia to count the debuff stacks shared on the target across all Assassins. Personal buffs remain character-specific.
- Updated the client effect catalog and tracking choices for skills that can apply both beneficial and harmful effects, including Earth Punishment.

Includes the features and fixes from 1.1.39.

## Validation and test notes

The 1.1.40 installer and native executable report version 1.1.40. Release build, built-browser UI checks, focused updater UI checks, and 213 Rust tests passed; two environment-specific tests were skipped. Please verify the next in-app update, padlock unlocking, boss-skill display modes, multiple same-class party members, and Insignia stacks in a live game session before wider release. Some effect and history coverage discrepancies remain under investigation.

Installer: `aion2t-dps-setup-1.1.40-x64.exe` (15,671,752 bytes).
SHA-256: `03a3fef3f6b38c2adfa65fff85c381f81bde03813c89e12df2154ea072b4c827`.
