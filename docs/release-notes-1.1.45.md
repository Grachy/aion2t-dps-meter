# Release 1.1.45

## Mini-map and controls

- Keep the chosen mini-map zoom when changing locations or layers, including transitions through unsupported maps and delayed character identification. Follow and recenter behavior is retained.
- Configure the mini-map **Pin/unpin** shortcut in Controls; the default is **Ctrl+M**. Show/hide remains a separate shortcut, **Ctrl+Shift+M** by default.
- Shortcut hints reflect saved bindings in all ten interface languages.
- Corrected Odyle labels and stabilized map resource popups, including outside-click and Escape handling.

## PvP and AUTO mode

- Compact PvP sections put your party, opponents and **Mine** in horizontal expandable controls.
- Personal **Slim** and visible-character count (**1-5**) now live in a separate sliders-icon menu to the right of **Mine**. The menu starts closed and closes on Escape, an outside click or leaving PvP.
- Personal display choices are retained independently of the main Slim setting. Controls remain usable while combat updates arrive.
- Premium users can configure independent idle resets for world bosses, ordinary monsters and PvP; saved choices are retained when Premium is unavailable.
- AUTO uses verified party/raid membership before merging combat and includes only your own training-dummy damage.
- Improved AUTO location classification: known PvE and quest instances cannot trigger PvP, while arenas and battlegrounds select PvP. Mixed world and Abyss locations still require combat evidence.
- Location changes invalidate stale PvP and boss context. Known quest NPCs no longer become false player targets in the reproduced case.

## Combat Assist and overlays

- Fixed Combat Assist losing its boss target after the game selection was cleared. With an empty selection, it can use the current registered living PvE boss. Explicit selections, PvP and invalid-target checks remain enforced.
- Ally cooldown choices remain available after cooldown expiry, combat reset and location changes, across all nine classes.
- Game-window following defaults to enabled. Improved hiding and restoring the meter with the game window.
- Added a transparent world-boss respawn table, corrected related labels, and put the current confirmed location first in Alerts.

## Known limitations

- Some other players' ordinary damage on crowded world bosses is still missing. This release **does not guarantee a complete damage ranking**, and no new Global rDPS accuracy fix is claimed.
- Map positions depend on network observations; resource and pet markers show known locations, not live availability.
- Fresh in-game checks of Combat Assist on a boss, target clearing, mini-map shortcuts and teleporting, PvP/AUTO transitions, dense combat and actual installation/update remain necessary before wider distribution.

## Validation and download

- **380 Rust tests passed; 7 skipped.**
- Full optimized release build and **23 obfuscated scripts** passed browser checks, including final assets after native processing.
- Verified **1,262 source files** and **853 final interface files** against saved hashes.
- Browser checks passed **12 mini-map zoom transitions** and **four startup cases**, including delayed rendering.
- Recorded native checks cover boss-assist selection, AUTO classification, verified parties, training damage and ally cooldown choices. Boss-assist regression includes the recorded Duanka packet.
- Npcap prerequisite checks passed all **10 installer languages** and three prerequisite cases.
- All **five** disposable tests of the generated installer restart callback and hooks passed.
- Native executable and installer metadata report **1.1.45**; the application is **Windows x64**. The release copy matches the built installer byte for byte.

Installer: [aion2t-dps-setup-1.1.45-x64.exe](aion2t-dps-setup-1.1.45-x64.exe) (26,069,429 bytes).

SHA-256: `fb56ccbb995aad45d755990ec5ced02b6fd0f209fe7f6cc9e355dcacaa1f07da`.
