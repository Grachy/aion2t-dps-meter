# Release notes: 1.1.47?1.1.49

Cumulative release notes for GitHub, including the October 26, 2026 rebuild of 1.1.49.

---

## Release 1.1.49

Updated Windows x64 installer — October 26, 2026. This rebuild includes the original 1.1.49 changes and the additions below.

**Already running an earlier 1.1.49 build? Download and run this installer manually. The version number is unchanged, so the updater will not offer it as a newer version.**

### Cloud Merchant

- Added a dedicated Cloud Merchant overlay and a toolbar button, with separate **Skins**, **Pets** and **Rare** tabs.
- Show missing skins when the character's collection is known, and pets that still need progression. Preserve verified skin collections per character; incomplete collection data is shown as unknown rather than treating every skin as missing.
- Display original item icons, skin grade colors and pet soul progress out of **105**. Rare pets use the selected rare-pet catalogue, including Dionae, Furious Feruk and Phantasmal Lakshmi.
- Refresh the rare-pet catalogue in already open windows so classification corrections appear without restarting the meter.
- Remove redundant pet prefixes and bound-item suffixes. Merchant alerts use three short counts: new skins, rare pets and ordinary pets, in the notification overlay.
- Added Premium-only background stock retrieval. Free users can open the in-game shop and switch its tabs to read stock; the last received list remains available after closing the shop until it expires.
- Handle stock arriving before character identification, show whether all categories have arrived, and remove successfully purchased goods from the current list.
- Added the Black Cloud Merchant stock-refresh timer, with a shorter label that fits the timer window.
- Bundle the merchant helper, verify its files before launching it and configure its Windows Firewall rule during installation. Background retrieval is disabled by default.

### Hidden cubes and support tools

- Added hidden-cube detection from received game packets, a dedicated overlay and a toolbar button.
- Track supported cube types, distance and disappearance, suppress duplicate alerts, and clear observations when changing characters or maps.
- Added **Record data for support** and **Save report ZIP** in Advanced settings. Recording can be started without restarting the meter.

### Combat, AUTO mode and party tracking

- Fixed AUTO switching to a stale boss after a kill, which could reset the visible result or create an incorrect extra fight.
- Preserve confirmed encounter participants through roster refreshes, including Cyrillic player names.
- Improved party/map retention when login data arrives late, and scoped dungeon identities to the current world instance. This addresses missing participants such as Saiton after changing zones.
- Prevent boss or summon effects from incorrectly identifying an NPC as the local player and disrupting fight selection or duration.
- Corrected Tamon's healing/absorption phase accounting, which could inflate player damage and DPS.
- Added support for the verified 10-versus-10 battlefield roster and opposing-team display.

### Boss respawns, siege timers and overlays

- Hide the boss respawn overlay when the game is minimized, absent or another application is active; restore it without taking focus when the game returns.
- Prioritize the character's home region in boss alerts: **Altgard for Asmodians** and **Verteron for Elyos**. Keep countdown ordering within each region and refresh the order after character changes.
- Corrected EU daylight-saving time handling and Watcher Kaira's respawn fallback.
- Use received siege timing data to correct the displayed schedule and notifications.
- Restore the **Choose bosses** shortcut after moving boss alerts into their own widget.
- Fixed new merchant/cube windows failing to open because their event permissions were missing.
- Added visible unlock hints using the configured shared shortcut and Alt+click.
- Premium feature selection now stays open while selecting multiple options.
- Fixed language updates in detached windows, including the Timers title, and shortened merchant timer text across supported languages.

### Global checklist

- Removed the EU-only restriction on typed checklist packets for **NA East, NA West, Europe, South America and Asia**.
- Bind readings to the confirmed character, region and server. Keep the legacy resource reader as a fallback and let validated typed records take precedence for base and bonus values.
- Preserve login observations that arrive before character identification and add checklist-binding diagnostics.

### Replays and dungeon gathering

- Corrected replay damage attribution for known effects and explicitly owned summons. Added a persistent option to include or exclude eligible non-boss adds.
- Recorded checks align six original replays and all thirty participant totals with fight history when adds are included. Original recordings and stored damage amounts are preserved.
- Restore validated cross-server members in dungeon gathering and preserve empty party slots.

### Validation and known limitations

- Optimized x64 build and NSIS packaging passed. **458 Rust tests passed; 7 were ignored**, and `cargo check` passed.
- The production UI passed browser checks with 31 obfuscated scripts. Verified 2,959 final asset hashes, 218 merchant runtime files, source inputs and executable/installer version metadata.
- Global checklist tests include synthetic region/ownership cases and recorded EU data. Fresh NAE values still need comparison with the game; the reported user's debug log did not contain full checklist packet bodies.
- Background merchant retrieval may require a fresh game connection if the meter starts after the game is already connected. Continuous hourly refresh and reconnect behavior still need live validation.
- Fresh live combat, cube detection, siege transitions and overlay behavior remain validation items. Other players' full ordinary damage at public bosses remains unresolved, including party/raid members.
- An alternative Invasion interval has not been verified; this build does not claim to fix that reported schedule discrepancy.

Includes all changes from 1.1.48 and 1.1.47. See the [combined release notes](release-notes-1.1.47-1.1.49.md).

Installer: [aion2t-dps-setup-1.1.49-x64.exe](aion2t-dps-setup-1.1.49-x64.exe) (77,277,269 bytes).

SHA-256: `f9d69acdde963b59605a4441e799c99048cee00ccddcd305d89f2792273eec7a`.

---

## Release 1.1.48

### Combat replays

- Show the boss on the map with a separate target card, HP/stagger tracks and one horizontal row of effects. Boss events appear below the map.
- Use compact party cards so the group fits better. Each player's effects show one row by default and can be expanded. Redundant coordinates below names are removed.
- Include original client icons, boss portraits and supported attack areas, plus recorded target and gauge events.

### Overlay windows

- Boss respawns and dungeon group windows now have a background-opacity icon (0–100%) and click-through lock button. Text and icons retain their opacity.
- Ctrl+M, or the saved custom binding, controls visible mini-map, mini checklist, activity timers, boss respawns and dungeon group windows together. Alt+click unlocks one window and consumes the complete gesture.
- Full-checklist opacity/lock controls are removed; its settings button is beside Close. Mini-checklist controls remain available.
- Retain legacy transparent boss backgrounds and independent saved opacity settings. Compact checklist settings open in a separate sidebar.

### Checklist, details and maps

- Mark weekly base limits complete even when bonus entries remain, including Daily Dungeon and Ascension Trial.
- Update shop/morph data and use client terminology and translated interface labels in ten languages.
- Improve fight-detail layout and readability, repair detached-window dragging, and retain each participant's class icon in history, including repeated classes.
- Use verified client resource-map candidates and item icons. Candidate locations do not mean all nodes spawn simultaneously.

### Installation and validation

- Interactive setup recommends Borderless Window or Window mode because Fullscreen does not display the overlay. Silent updates skip this message; Npcap prerequisite checks remain.
- Optimized x64 native build and NSIS packaging succeeded. The final build passed the full browser suite with 28 obfuscated modules; 1,725 source files, 1,286 final assets and version metadata were verified.
- Prior native/recorded checks are retained, including forty isolated Alt-click cycles and all four tool-window slots. They were not rerun solely for packaging.
- Replay capture/combat collection changed; verify boss targets, stagger, effects and attack areas against fresh live capture before wider distribution. Physical Ctrl+M/Alt+click and the interactive installer notice also need in-game/interactive checks.
- Other players' full ordinary damage at public bosses remains unresolved, including party/raid members.

Includes previous 1.1.47 party-damage and Alt+click fixes.

Installer: [aion2t-dps-setup-1.1.48-x64.exe](aion2t-dps-setup-1.1.48-x64.exe) (31,060,541 bytes).

SHA-256: `a2559224c0b39f0abed5454cc232780f920ad952861bd3d162315768d5f0d48e`.

---

## Release 1.1.47

### Dungeon party damage

- Fixed party members being excluded from the damage table when the compressed party list was interpreted incompletely. The issue can affect any class or party composition, including two players of the same class.
- Use the complete verified roster in the current dungeon. Players remain separate; uncertain identities or conflicting servers are not merged.
- AUTO now counts the first eligible party hit, including several opening hits arriving between screen updates.
- The meter, boss details and new saved fights use the same participant scope. Existing saved history is not rewritten.

### Alt+click unlocking

- Improved Alt+left-click unlocking for the main HUD and mini-map.
- Unlock on the press and handle its matching release, including releasing Alt before the mouse button.
- Prevent the same gesture from immediately locking the window again. Existing hotkey bindings are retained.
- Respect hidden, minimized and covered windows.

Includes all previous 1.1.46 changes, including the final Combat Assist cooldown-reset and buff-selection fixes.

### Validation and limitations

- 398 Rust tests passed; 7 ignored, plus cargo check. These checks cover the unchanged source included in this installer and were not repeated solely for packaging.
- Three original recorded dungeon fights were replayed in six configurations. All five participants and exact boss damage totals were preserved, including the missing player's opening hits.
- Native Alt+click routing passed 40 isolated Windows cycles. The fresh release build passed the full browser suite for 27 obfuscated scripts, including early Alt release; all 883 final asset hashes match the checked build.
- Verified 1,306 source files, 14 previously checked fix-source/fixture hashes, five snapshot versions and native/installer metadata as 1.1.47. Optimized x64 native compilation and NSIS packaging succeeded.
- One recorded Nuakum replay omits its initial NPC spawn: live rows were checked against raw hits at the last pre-death update, while final details/history totals were checked against all recorded hits.
- Fresh in-game five-player combat, physical Alt+click and focus/restore checks remain before wider distribution. Other players' full ordinary damage at public bosses remains unresolved, including party/raid members.

Installer: [aion2t-dps-setup-1.1.47-x64.exe](aion2t-dps-setup-1.1.47-x64.exe) (29,369,415 bytes).

SHA-256: `f12d3b501cc0d437253d29240b9fae0571647c3a1102510731757d1bffef29b6`.
