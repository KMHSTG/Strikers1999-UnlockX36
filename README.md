# **Strikers 1999 / 1945-III - Unlock X-36**

This patch makes the X-36 unlocked by default in the Strikers 1999 MAME rom. It has no other effect. The advantage to unlocking the X-36 in this manner, as opposed to using the built-in password, is mainly that you will be able to record and playback Strikers 1999 demos in MAME with all ships, while disabling nvram. Which will let you avoid demo desync. After patching your rom, make sure to add the following command to both your recording and playback shortcuts (and any other shortcuts you will be launching the game with):  

If using Shmupmame 4.2:  -nvram_directory nul          
Example: \Shmupmameui_v42.exe s1945iii -record strikersdemo.inp -nvram_directory nul

If using regular MAME:    -nonvram_save                 
Example: \mame.exe s1945iii -record strikersdemo.inp -nonvram_save  

Before launching the patched game like this, make sure your MAME nvram directory has no "s1945iii" folder in it. If you make a mistake with your shortcuts, and run the game even once without the nvram-disable, then MAME will immediately recreate the s1945iii folder in the nvram directory. Preventing the s1945iii folder from ever appearing there, should be your visual aid on how to avoid demo desync with certainty.

## Patching Instructions:

1 - Extract your MAME Strikers 1999 rom archive (s1945iii.zip)

2 - Using your xdelta patcher of choice, apply the strikers-x36.xdelta patch to the file named "eeprom-s1945iii.bin". Make sure that your patched file has the same filename as the original.

3 - Rezip the Strikers 1999 rom archive.
  
  
##### NOTE: When you start up the patched rom, MAME will complain about wrong checksum. This is expected, and can be safely ignored. If necessary, the patching process can be verified using the hashes below:
  
eeprom-s1945iii.bin

(Original) &nbsp; CRC32:&nbsp; b39f3604  
(Original) &nbsp; MD5:  &nbsp; &nbsp;   6adaad093d12ccf7aa28cef9f47412e6  
(Original) &nbsp; SHA-1: &nbsp; d7c66210598096fcafb20adac2f0b293755f4926  
  
(Patched) &nbsp; CRC32:&nbsp; 05ff62bb  
(Patched) &nbsp; MD5:  &nbsp; &nbsp;   9727640eb06674d0baa55a1ce12da779  
(Patched) &nbsp;  SHA-1: &nbsp; 06e193ba5cfb7f56eb10ed755de91b483104048a  

## &nbsp;

Patch by KMH  
2023-04-17 - Released
