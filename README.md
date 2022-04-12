## Gameboy Advance Sleep Mode Fixes for EZ-Flash Flashcarts

### Sleep mode issues

Although there exist sleep patches that can be applied to any game (including the ones built-in to the EZ-Flash IV fw2.x and EZ-Flash Omega), these often bring compatibility issues - with many games failing to work at all, or developing strange faults like failing to work reliably during serial comms in multiplayer mode.

Many first-party Nintendo GBA games do contain their own native sleep mode functions, but these don't work properly when using an EZ-Flash flashcart. They will wake the GBA instantly when engaged, apparently because EZ-Flash devices generate spurious gamepak interrupts.

### Fixes for native sleep modes
Back in the day, ROM patches were figured out to fix many of these games to ignore these additional interrupts. This was difficult information to track down in the present day: 

https://web.archive.org/web/20180904111600/https://ezflash.sosuke.com/viewtopic.php?f=16&t=12662 
https://web.archive.org/web/20180904023246/https://ezflash.sosuke.com/wiki/index.php?title=GBA_sleep_mode 

These patches were originally published in a rather non-standard way, depending on a Windows binary tool called hexalter.

### My improvements
- Patches converted to IPS patches, cross-platform
- Additional patches where some variants or regions of the game were missing
- Added the crc32 checksum of the target ROM file to each patch filename, for validation

### Additional reading
- [Idle loop patches at GBATEMP forum](https://gbatemp.net/threads/game-boy-advance-idle-loop-patches-i-e-speedhacks.396278/) to reduce battery consumption for some games
