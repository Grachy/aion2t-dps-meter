# Release 1.1.54

- Improve recovery when changing instances with ExitLag or other loopback-based accelerators. Capture new connection starts before the socket discovery filter catches up, while requiring current game-process ownership before parsing.
- Preserve bounded TCP framing and queued packets through temporary ownership-table gaps. Pause protocol timeouts during those gaps so partial character/name packets and out-of-order continuations can resume correctly.
- Allow a previously selected connection to resume after the active instance disappears, requiring fresh own-character evidence and suppressing earlier combat from that stream.
- Handle TCP SYN/SYN-ACK when an endpoint tuple is reused. Duplicate handshake packets do not reset a new stream, and other connections keep their independent state.
- Keep concrete game-owned half-open and half-closed TCP connections available to capture instead of treating every non-ESTABLISHED row as missing ownership.
- Make the target GS/CP panel follow the independent PvP settings. Retain the previous performance, merchant, Premium, hotkey and cube-direction fixes.

## Validation

The reconnect source passed 546 native tests,2 additional installed Npcap offline checks, cargo check and the original six recorded fights/all 30 player rows. On 26 repeated-connection intervals extracted from the two customer logs, synthetic fragmented identity probes recovered 26/26 with the fix versus 0/26 with the original transport; subsequent damage and buffs also passed. The logs do not contain the original TCP packets, so this is not a complete replay of the customer session or proof of its exact cause.

For packaging, the frontend was rebuilt and 33 modules obfuscated; built frontend checks, all 154 helper file hashes, EXE/installer versions and SHA-256 were verified. Previously completed native tests were reused. Capture/identity admission changed: fresh direct and ExitLag instance transitions, names, DPS and Combat Assist still need live verification before broad publication.

Installer: [aion2t-dps-setup-1.1.54-x64.exe](aion2t-dps-setup-1.1.54-x64.exe) (44,743,721 bytes).

SHA-256: b398a67c074da31683da475dbd08767168c771900e244c222a4046479035a9a7.
