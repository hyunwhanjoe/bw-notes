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
When I am on the bottom position the mineral address is StarCraft.exe+17F0F0 (0x57F0F0) and StarCraft.exe+17F0F4 at the top position.  
The mineral addresses seem to go up by 4 bytes.  
It seems that the address for StarCraft.exe is 0x400000.

Lost Temple has 4 positions: 12, 3, 6, 9 o'clock  
The mineral address StarCraft.exe+17F0F0 is used for 9 o'clock  
StarCraft.exe+17F0F4 is used for 6 o'clock  
StarCraft.exe+17F0F8 is used for 12 o'clock  
StarCraft.exe+17F0FC is used for 3 o'clock  
This matches when opening the map with StarEdit.exe in the Starcraft folder.  
Player 1 Red is at 9 o'clock and so on.

Create a single player game on Astral Balance.  
(New/first) scan for the player number based on your position. For example you are player 2 if you are on top and player 1 if on bottom. Keep making a new game and (next) scan based on your player number. Eventually after switching player numbers you will find two addresses.  
StarCraft.exe+17F0B0 (0x57F0B0)  
StarCraft.exe+19B460  
These two addresses seem to keep track which player number you are.  
If during a game you read your player number from 0x57F0B0, subtract your player number by one, multiply by 4 and add by 0x57F0F0, then you can automatically calculate your mineral address.  
