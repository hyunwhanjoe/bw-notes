I used cheat engine for this which can be downloaded [here](https://www.cheatengine.org/downloads.php)  
Clicking on the download link doesn't seem to download anything for me. I had to go to the link to download it.  
Deselect any additional/optional programs when installing.  

First select and open brood war in cheat engine.  
I used chaos launcher to run brood war in windowed mode.  
Create a single player game on Astral Balance.  
(New/first) Scan for the value 50. After training a peon and spending your minerals (next) scan for the value 0.  

The scan found three memory addresses.  
The value of the 2nd and 3rd addresses revert back to the original value after changing them.  
So the first address is the address holding the mineral value.

The map Astral Balance only has a top and bottom position.  
When I am on the bottom position the mineral address is StarCraft.exe+17F0F0 and StarCraft.exe+17F0F4 at the top position.  
It seems that the address for StarCraft.exe is 0x400000.

Lost Temple has 4 positions: 12, 3, 6, 9 o'clock  
The mineral address StarCraft.exe+17F0F0 is used for 9 o'clock  
StarCraft.exe+17F0F4 is used for 6 o'clock  
StarCraft.exe+17F0F8 is used for 12 o'clock  
StarCraft.exe+17F0FC is used for 3 o'clock  
This matches when opening the map with StarEdit.exe in the Starcraft folder.  
Player 1 Red is at 9 o'clock and so on.
