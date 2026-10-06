# Release 1.1.39

## New features

- Added optional automatic DPS reset after a configurable period of inactivity. Disabled by default; enable it in DPS settings and choose your timeout.
- Added support for installed 64-bit SAPI 5 voices, including voices exposed through compatible SAPI adapters. Fixed silent native voice previews.

## Bug fixes and improvements

- Restored screenshot copying on the meter's copy button, with a confirmation after the image is copied to the clipboard. Text results remain available through the configurable hotkey (Ctrl+Z by default).
- Fixed auto-reset being cancelled when live target data disappeared but the last fight remained on screen.
- Fixed Combat Assist and notification overlays disappearing when unlocked for placement. Improved position preservation when window or notification sizes change.
- Fixed invalid Focused Block charge values producing counters such as 16/16.
- Improved cooldown tracker cleanup to reduce state buildup during long sessions.
- Improved ping compatibility with Npcap devices that support synchronized low-precision timestamps but lack high-precision timestamp support.
- Simplified the world-boss timer button to an icon; boss details remain in its tooltip and timer panel.

Includes the features and fixes from 1.1.38.

## Notes

Voice availability depends on 64-bit SAPI registration. Ping precision depends on the supported Npcap clock mode. Affected-user ping and extended-session performance still need live validation.

Validation: release build, built-browser UI checks and 206 Rust tests passed; two local SAPI/Npcap integration tests were skipped. Native EXE and installer versions, installer contents and SHA-256 were verified.

Installer: `aion2t-dps-setup-1.1.39-x64.exe` (15600390 bytes).
SHA-256: `f3d69af4fe00bb95fe139b0441a02c21f7d7e25ffee31b30ab800ca0326e1099`.
