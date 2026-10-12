# Release 1.1.41

## New features

- **Character checklist:** track daily and weekly activities, Odyle Energy, tickets, keys and purchase limits. Character tabs show the class, name and Odyle balance, with a clear indication of whose activities are selected.
- **Detailed activity counters:** expand Command purchases, Arena, Battlefield and Daeva Pass EXP to see their individual limits. Additional counters show Abyss Points and the three Abyss Corridors.
- **Shop purchase tracking:** Wind Breeze Merchant Odyle purchases are tracked separately from Substance Morph, with their own server and character limits. Added Resurrection Spiritstone, seasonal Spiritstone, Soul Crystal and Daily Dungeon instant-clear ticket limits.
- **Pet farming map:** find soul-farming locations for pets that have not reached level 3. Includes Verteron, Altgard and Chaotic Lower Reshanta, per-character collection progress, search, zoom, spawn details and a player-position marker.

## Fixes and improvements

- Fixed checklist readings being assigned to the wrong character during character switches.
- Fixed completed daily and weekly activities remaining marked as done after the game's reset. Expired readings now require fresh game data instead of displaying old progress.
- Fixed Command totals hiding already-read purchases until every shop had been visited. Known purchases stay visible while unread limits are marked as unknown.
- Improved packet capture on VLAN-tagged connections, including affected Intel Wi-Fi setups.
- Fixed boss identity and fight duration when the game reuses NPC IDs, improved Unicode character-name handling, and fixed nickname sizing when resizing the overlay.
- Updated the checklist with original game icons, square corners and the meter's familiar dark gray appearance.

## Installation

The installer now checks for **Npcap**. If it is missing, it links to the official download and lets you retry after installing it. Npcap must be installed with **WinPcap API-compatible Mode** enabled. Cancelling the prerequisite check stops the meter installation.

## Known limitations

- The pet map shows spawn locations, not live mob availability or respawn countdowns. Pet collection changes may require a new character login to refresh.
- The Pet Auto-Loot Voucher purchase limit is not yet mapped and may show **—**. Unread counters remain unknown rather than being shown as zero.

## Validation

Native executable and installer versions verified as **1.1.41**. Release build and built-browser UI checks passed. The source passed **256 Rust tests** (5 skipped), focused checklist/map checks, and isolated Npcap prerequisite checks. Live map movement, character switching and installation on a clean Windows machine remain recommended checks before wider distribution.

Installer: `aion2t-dps-setup-1.1.41-x64.exe` (24,542,867 bytes).

SHA-256: `fc8d75f4365253a317392d5d67732efbfef22fb76cc636738445b5d850d34a34`.
