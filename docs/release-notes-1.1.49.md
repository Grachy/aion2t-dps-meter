# Release 1.1.49

Updated Windows x64 installer — October 26, 2026. This rebuild includes the original 1.1.49 changes and the additions below.

**Already running an earlier 1.1.49 build? Download and run this installer manually. The version number is unchanged, so the updater will not offer it as a newer version.**

## Cloud Merchant

- Added a dedicated Cloud Merchant overlay and a toolbar button, with separate **Skins**, **Pets** and **Rare** tabs.
- Show missing skins when the character's collection is known, and pets that still need progression. Preserve verified skin collections per character; incomplete collection data is shown as unknown rather than treating every skin as missing.
- Display original item icons, skin grade colors and pet soul progress out of **105**. Rare pets use the selected rare-pet catalogue, including Dionae, Furious Feruk and Phantasmal Lakshmi.
- Refresh the rare-pet catalogue in already open windows so classification corrections appear without restarting the meter.
- Remove redundant pet prefixes and bound-item suffixes. Merchant alerts use three short counts: new skins, rare pets and ordinary pets, in the notification overlay.
- Added Premium-only background stock retrieval. Free users can open the in-game shop and switch its tabs to read stock; the last received list remains available after closing the shop until it expires.
- Handle stock arriving before character identification, show whether all categories have arrived, and remove successfully purchased goods from the current list.
- Added the Black Cloud Merchant stock-refresh timer, with a shorter label that fits the timer window.
- Bundle the merchant helper, verify its files before launching it and configure its Windows Firewall rule during installation. Background retrieval is disabled by default.

## Hidden cubes and support tools

- Added hidden-cube detection from received game packets, a dedicated overlay and a toolbar button.
- Added eight-way map directions beside hidden-cube distances in the widget and notifications. Directions update with player position and are hidden when position data is stale or unavailable; arrows follow map north, not camera rotation.
- Track supported cube types, distance and disappearance, suppress duplicate alerts, and clear observations when changing characters or maps.
- Added **Record data for support** and **Save report ZIP** in Advanced settings. Recording can be started without restarting the meter.

## Combat, AUTO mode and party tracking

- Fixed AUTO switching to a stale boss after a kill, which could reset the visible result or create an incorrect extra fight.
- Preserve confirmed encounter participants through roster refreshes, including Cyrillic player names.
- Improved party/map retention when login data arrives late, and scoped dungeon identities to the current world instance. This addresses missing participants such as Saiton after changing zones.
- Prevent boss or summon effects from incorrectly identifying an NPC as the local player and disrupting fight selection or duration.
- Corrected Tamon's healing/absorption phase accounting, which could inflate player damage and DPS.
- Added support for the verified 10-versus-10 battlefield roster and opposing-team display.

## Boss respawns, siege timers and overlays

- Hide the boss respawn overlay when the game is minimized, absent or another application is active; restore it without taking focus when the game returns.
- Prioritize the character's home region in boss alerts: **Altgard for Asmodians** and **Verteron for Elyos**. Keep countdown ordering within each region and refresh the order after character changes.
- Corrected EU daylight-saving time handling and Watcher Kaira's respawn fallback.
- Use received siege timing data to correct the displayed schedule and notifications.
- Restore the **Choose bosses** shortcut after moving boss alerts into their own widget.
- Fixed new merchant/cube windows failing to open because their event permissions were missing.
- Added visible unlock hints using the configured shared shortcut and Alt+click.
- Premium feature selection now stays open while selecting multiple options.
- Fixed language updates in detached windows, including the Timers title, and shortened merchant timer text across supported languages.

## Global checklist

- Removed the EU-only restriction on typed checklist packets for **NA East, NA West, Europe, South America and Asia**.
- Bind readings to the confirmed character, region and server. Keep the legacy resource reader as a fallback and let validated typed records take precedence for base and bonus values.
- Preserve login observations that arrive before character identification and add checklist-binding diagnostics.

## Replays and dungeon gathering

- Corrected replay damage attribution for known effects and explicitly owned summons. Added a persistent option to include or exclude eligible non-boss adds.
- Recorded checks align six original replays and all thirty participant totals with fight history when adds are included. Original recordings and stored damage amounts are preserved.
- Restore validated cross-server members in dungeon gathering and preserve empty party slots.

## Validation and known limitations

- Optimized x64 build and NSIS packaging passed. **459 Rust tests passed; 7 were ignored**, and `cargo check` passed.
- The production UI passed browser checks with 31 obfuscated scripts. Verified 2,959 final asset hashes, 218 merchant runtime files, source inputs and executable/installer version metadata.
- Global checklist tests include synthetic region/ownership cases and recorded EU data. Fresh NAE values still need comparison with the game; the reported user's debug log did not contain full checklist packet bodies.
- Background merchant retrieval may require a fresh game connection if the meter starts after the game is already connected. Continuous hourly refresh and reconnect behavior still need live validation.
- A real hidden-cube packet and eight simulated player offsets passed direction checks. Fresh live combat, on-screen cube directions, siege transitions and overlay behavior remain validation items. Other players' full ordinary damage at public bosses remains unresolved, including party/raid members.
- An alternative Invasion interval has not been verified; this build does not claim to fix that reported schedule discrepancy.

Includes all changes from 1.1.48 and 1.1.47. See the [combined release notes](release-notes-1.1.47-1.1.49.md).

Installer: [aion2t-dps-setup-1.1.49-x64.exe](aion2t-dps-setup-1.1.49-x64.exe) (77,285,119 bytes).

SHA-256: `3403275125b396dc869916a0482669b6f4c0b3e5eb5d507b04d6e72fef289cb7`.
