# pisend
pisend betas

07/05/2002 pisend v2.20    Raindbow Player (i2s.bin) v1.1 

This is just an update for the visualizer , Raindbow Player 


-- known issues 
  - still may crash 
  
-- updates
  - added help with H 
  - faster visuals 
  - press N to load a new tune from the 

01/05/2020 v2.20

I HIGHLY recommend you now use 2mbit unles you have an issue. There is a try2mb.bas file in the pisend folder that will let you TEST the faster speeds - you can revert by doing a power cycle. Everything is better at 2mb!

-- known issues 

  - visusliser crashes randomly, recommend a reset for now.

-- updates 
  - added more visual things (even more sickly)
  - now tries to read meta data for the file from SD or asking the pi0
    (this isnt 100% failure proof)
  - Now plays track time in pi0 player offers it up
  - improves larger tranfers
  - some internal improvements to pisend 
  - updated handlers for new visuals 
-- fixes 
  - many 
  - more
  
22/03/2020

-- updates 
  - added more visual things 
  - added mp3 player
-- fixes 
  - drops speed to allow uart to keep pace
  - fixes files >4MB that could faile. tested many files up to 20mb.

09/03/2020

-- updates
  - added visualisers to audio playback
  - tzxload now adjusts playback frequency to match timings 
  - fixed missing quotted file names with spaces in SDH and SID players (eugh)

v2.06b 01/03/2020

-- fixes 
  - now reserves and free banks then restores

updates
  - added -s for soft key (no clear of console)
  - added -r to empty 512 bytes to $c000 fron the uart buffer 
  - clean up interface

includes some updated handlers for mod/xm, sid, sndh, tzx 

first version of ModPi Player included with better playback control & amplification 



usage
```
.pisend -q 

 tests for NextPi, first 115,200 then 2Mbit, sets ref $7f to 2 or 8 respectively, 0 on fail
 
.pisend {filename}

 base64 encodes the selected file and sends in chunks to NextPi
 
.pisend -s {string}

 sends keys to NextPi console (useful for controlling running apps like ModPi)
 
 You must .pisend -q before .pisend -U as this will set an internal register.
 
.pisend -U 
 ** WARNING THIS COULD STOP NEXTPI FROM BOOTING **
 swaps baud rate of NextPi between 115,200 and 2Mbit, reboots the pi. Use .term to check progress
 
 ```
 The update hasnt failed in any test but as it is altering a boot file, the warning is given
 
 
 
 
 
