# gba-ezflash-sleep-fixes
Fixes for Gameboy Advance games with built-in sleep modes when running on EZ Flash flashcarts

Like the [GBATEMP forum thread](https://gbatemp.net/threads/game-boy-advance-idle-loop-patches-i-e-speedhacks.396278/) about idle loop fixes, what follows here is more information that was lost with the demise of the ezflash.sosuke.com forum.

Although the newer 2.0x firmwares for the EZ-FLASH IV contain a sleep patcher (GSS), this more often than not brings its own compatibility issues - with many games failing to work at all, or developing strange faults like failing to work reliably during serial comms in multiplayer mode.

However, many first party Nintendo GBA games contain their own sleep mode functions, but these don't work properly when using an EZ-FLASH IV. They will wake the GBA instantly when engaged, apparently because the EZ-FLASH generates spurious gamepak interupts. Back in the day, ROM patches were figured out to fix many of them. This was difficult information to track down in the present day.
https://web.archive.org/web/20180904111600/https://ezflash.sosuke.com/viewtopic.php?f=16&t=12662
https://web.archive.org/web/2018090...osuke.com/wiki/index.php?title=GBA_sleep_mode

The format used for these patches was rather non-standard, depending on a Windows binary tool called hexalter. I decided to read up on the specification for IPS patches, and convert them so they're a bit more cross-platform friendly. I have also added a few more patches where some variants or regions of the game were missing. Since the Good ROM tools and their naming conventions seem to have disappeared I have added the crc32 checksum of the target ROM file to each IPS patch filename, so that you can verify that you have the specific ROM version which each patch expects.

Here are the games which can be fixed, IPS patches for each are provided:

Baldur's Gate - Dark Alliance (E)
Baldur's Gate - Dark Alliance (U)
Bit Generations Dial Hex (J)
Dr. Mario & Puzzle League (E)
Dr. Mario & Puzzle League (U)
Drill Dozer (U)
Legend of Zelda, The - A Link To The Past Four Swords (E)
Legend of Zelda, The - A Link To The Past Four Swords (U)
Legend of Zelda, The - The Minish Cap (E)
Legend of Zelda, The - The Minish Cap (U)
Metroid - Zero Mission (E)
Metroid - Zero Mission (U)
Metroid Fusion (E)
Metroid Fusion (U)
Mother 3 (J)
Scurge - Hive (E)
Super Mario Advance 3 - Yoshi's Island (E)
Super Mario Advance 3 - Yoshi's Island (U)
Super Mario Advance 4 - Super Mario Bros. 3 (E)
Super Mario Advance 4 - Super Mario Bros. 3 (E) (Rev 1)
Super Mario Advance 4 - Super Mario Bros. 3 (U)
Super Mario Advance 4 - Super Mario Bros. 3 (U) (Rev 1)

Enjoy!
