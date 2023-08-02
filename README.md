## Gameboy Advance Sleep Mode Fixes for EZ-Flash Flashcarts

### Sleep mode issues

Sleep patches that can be applied to any GBA game already exist (including the ones built-in to the EZ-Flash IV fw2.x and EZ-Flash Omega), however these often cause compatibility issues. Many games will fail to work at all, or may fail serial communications during multiplayer mode.

Many first-party Nintendo GBA games do contain their own native sleep mode functions, but these don't work properly when using an EZ-Flash flashcart. They will wake the GBA instantly when sleep is engaged, apparently because EZ-Flash devices generate spurious gamepak interrupts.

### Fixes for native sleep modes
Back in the day, ROM patches were figured out to fix many of these games for EZ-Flash. This was difficult information to track down, some 14 years later: 

https://web.archive.org/web/20180904111600/https://ezflash.sosuke.com/viewtopic.php?f=16&t=12662 
https://web.archive.org/web/20180904023246/https://ezflash.sosuke.com/wiki/index.php?title=GBA_sleep_mode 
https://gbatemp.net/threads/classic-nes-sleepmode-working-on-ez-flash-iv.433762/ 

These patches were originally published in a rather non-standard way, dependent on a Windows binary tool called hexalter.

### My improvements
- Patches converted to IPS format, to allow cross-platform tools
- Added the crc32 checksum of the target ROM file to each patch filename, for validation
- Additional patches where some revision or region variant of the game was missing
- Created new patches for all Famicom Mini series titles, except those already created in the forum posts linked above (Vols. 11, 17, 18, 21) and several trickier ones which enable sleep from ARM code running in VRAM rather than by directly executing Thumb instructions from ROM (Vols. 04, 05, 09, 10 by [TechieSaru](https://gbatemp.net/threads/native-sleep-mode-fix-patches-for-ez-flash-iv.608648/post-10216389)).

### Additional reading
- [Idle loop patches at GBATEMP forum](https://gbatemp.net/threads/game-boy-advance-idle-loop-patches-i-e-speedhacks.396278/) to reduce battery consumption for some games
- [Classic NES Series / Famicom Mini patches at GBATEMP forum](https://gbatemp.net/threads/how-can-these-roms-be-made-to-work-with-the-ezflash-iv.378837/) to get these titles saving correctly on flashcarts (not needed for Famicom Mini Vols. 01-10).
