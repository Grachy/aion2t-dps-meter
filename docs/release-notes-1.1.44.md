# Release 1.1.44

## PvP and arenas

- The default PvP view shows your verified five-player party. Opponents, personal statistics and the full raid can be expanded when needed.
- Expanded raids use four groups of five arranged in two columns, instead of one long list.
- Collapse your own team directly from its header to focus on opponents.
- Fixed opponent detection for recorded **1v1** and **5v5** arena room formats.
- Improved current-HP decoding and death updates. Main PvP rows receive updates every **500 ms**, and older updates cannot restore a stale HP value after a death.
- The separate team overlay now requires explicit opt-in. Main team rows show health without effect icons, avoiding the unwanted extra team block and its icons.

## Fight history and damage

- Added a dedicated **World bosses** history tab with a flat list, without a repeated section heading for each boss.
- Moved history reads off the native UI thread and reduced metadata work. Stale requests are discarded to improve responsiveness when opening, changing or closing history views.
- Protected validated player names against stale class-based replacements. The protection applies across classes.
- Corrected ownership of supported aura, periodic, trap and summoned-entity damage across classes, using shared rules in the live meter, details and history. Ambiguous ownership remains unassigned.
- Fixed a reset-acknowledgement race that could leave the compact meter empty while native combat data was available.

## Mini-map

- Fixed opening the mini-map without relogging or teleporting when map and position data had already arrived.
- Improved position recovery during flight, reducing long freezes until landing in the recorded flight case. Recovered positions remain approximate.

## Known limitations

- Some other players' ordinary damage on crowded world bosses is still missing. This release **does not guarantee a complete damage ranking**, and no new Global rDPS accuracy fix is claimed.
- Map positions depend on available network observations; resource and pet spawn markers show known locations, not live availability.
- Fresh live checks of PvP health/opponents, flight, dense Abyss combat, transitions and the actual installation/update flow remain necessary before wider distribution.

## Validation and download

- **366 Rust tests passed; 7 skipped.**
- Full optimized release build and **23 obfuscated scripts** passed browser checks, including final assets after native CSS processing.
- Recorded native/replay checks cover arena rosters, death updates, flight recovery and shared effect damage. Across **19 complete recorded fights**, named-player live/details/history damage agreed.
- Verified **1,259 source files** and **854 final interface files** against their saved hashes.
- Npcap prerequisite checks passed installed, missing and actual-driver cases in all **10 installer languages**.
- All **five** disposable tests of the generated installer restart callback and hooks passed.
- Native executable and installer metadata report **1.1.44**; the application is **Windows x64**. The release copy matches the built installer byte for byte.

Installer: [aion2t-dps-setup-1.1.44-x64.exe](aion2t-dps-setup-1.1.44-x64.exe) (26,038,871 bytes).

SHA-256: `c8f2e8294601b16c77cf88ce0eb216e7ec1c9a08472b10612b1066d1c1cb7e59`.
