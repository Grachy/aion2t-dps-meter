# Release 1.1.50

## Damage and AUTO mode

- Attribute damage from objects with confirmed owners to their characters, including summoned objects and persistent effects. Recorded coverage includes all eight classes; equal boss intervals for the reported Atiel fight match Questlog totals for Pl and Inyron.
- In AUTO without a party, expand the local player's skill damage across current targets. Restore party rows when a party is detected.

## Controls, Premium and overlays

- Preserve rebound or disabled reset shortcuts across restart and serialize shortcut updates.
- Show Premium refresh progress, success/errors and effective access; provide relink guidance when appropriate. The exact cause of the reported Premium drop remains unproven.
- Show merchant helper startup, waiting-login, ready and error states. Match merchant actions and Open replays buttons to the application style.
- Include the current hidden-cube compass, Premium merchant access and compact helper improvements.

## Merchant regions and factions

- Accept both Light and Dark merchant categories, including the Light 101/104 responses in the affected NAE recording. Scope stock completeness to one faction.
- Pass confirmed faction categories to the helper for NAE, NAW, EU, SA and AS. Unknown categories do not trigger speculative requests.
- Native parsing and bundled helper are updated together.

## Validation and limitations

- cargo check, 468 Rust tests (7 ignored), 69 Python tests, final browser UI checks and NSIS packaging passed. Verified 154 bundled runtime files and installer metadata/checksum.
- Capture/combat parsing and ownership attribution changed. Recorded packet checks passed; fresh in-game checks remain before wider distribution, including merchant stock on the affected NAE client. The packaged NAE driver/live scenario is not yet verified.
- This installer replaces the earlier local 1.1.50 build. Existing 1.1.50 users must run it manually because the numeric version is unchanged.

Includes prior 1.1.49 fixes. Historical installers and release notes are preserved.

Installer: [aion2t-dps-setup-1.1.50-x64.exe](aion2t-dps-setup-1.1.50-x64.exe) (44,111,548 bytes).

SHA-256: `fe68ec4889311bcfea0cb92f599d4f8549f83aacc9632360dd029db82d567cde`.
