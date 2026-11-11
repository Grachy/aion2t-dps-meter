# Release 1.1.59

- Fix a Windows graphics-resource leak when resizing frameless windows and widgets.
- Avoid repeatedly raising already-topmost overlay windows and reduce repeated game-window enumeration.
- Keep ordinary AUTO farming damage and totals within the latest 10 minutes; keep PvP damage within the latest 20 minutes. Protect boss fights and overlapping combat data until the corresponding fight is saved successfully.
- Bound simultaneous fight-detail requests to prevent queued work from growing during repeated refreshes.
- Fix delayed personal-table updates and stale mob totals when AUTO switches to a boss.

Installer: [aion2t-dps-setup-1.1.59-x64.exe](aion2t-dps-setup-1.1.59-x64.exe) (44,891,701 bytes).

Mirrors: [Yandex Disk (1.1.59)](https://disk.yandex.com/d/kUxWNwC7pWj-Jg) · [Mega (1.1.59)](https://mega.nz/file/vaYxBDZJ#uGtYbKGEX7_LMlSEjA1eBrYOmq6kjAyL_lsznN5P20w).

SHA-256: e27c6c8fabe82c0672fc9031d291b92f367cb9f15db15d715783aa069d7795a4
