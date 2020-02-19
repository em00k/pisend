# pisend
pisend betas

v2.00b 19/2/2020

includes some updated handlers for mod/xm, sid, sndh, tzx 

first version of ModPi Player included with better playback control & amplication 

usage

.pisend -q 

 tests for NextPi, first 115,200 then 2Mbit, sets ref $7f to 2 or 8 respectively, 0 on fail
 
.pisend {filename}

 base64 encodes the selected file and sends in chunks to NextPi
 
.pisend -s {string}

 sends keys to NextPi console (useful for controlling running apps like ModPi)
 
.pisend -U 
 ** WARNING THIS COULD STOP NEXTPI FROM BOOTING **
 swaps baud rate of NextPi between 115,200 and 2Mbit, reboots the pi. Use .term to check progress
 
 The update hasnt failed in any test but because it is altering a boot file the warning is given
 
 
 
 
 
