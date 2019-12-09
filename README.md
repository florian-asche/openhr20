Openhr20
============

Detailed description and tutorial is avialable on the blog:
https://piontecsmumble.wordpress.com/

Clone of openhr20 project.

Added features:
- Added command O to open the HR20 (set max temp)
- Added command C to close the HR20 (set min temp)
- changed max temp to 40 degree celcius
- changed rs232 output to better readable with newline


All commands:
 *  \note commands have FIXED format
 *  \note command X.....\n    - X is upcase char as commad name, \n is termination char
 *  \note hex numbers use ONLY lowcase chars, upcase is reserved for commands
 *  \note   V\n - print version information
 *  \note   D\n - print status line 
 *  \note   Taa\n - print watched variable aa (return 2 or 4 hex numbers) see to \ref watch.c
 *  \note   Gaa\n - get configuration byte with hex address aa see to \ref eeprom.h 0xff address returns EEPROM layout version
 *  \note   Saadd\n - set configuration byte aa to value dd (hex)
 *  \note   Rab\n - get timer for day a slot b, return cddd=(timermode c time ddd) (hex)
 *  \note   Wabcddd\n - set timer  for day a slot b timermode c time ddd (hex)
 *  \note   B1324\n - reboot, 1324 is password (fixed at this moment)
 *  \note   Yyymmdd\n - set, year yy, month mm, day dd; HEX values!!!
 *  \note   Hhhmmss\n - set, hour hh, minute mm, second ss; HEX values!!!
 *  \note   Axx\n - set wanted temperature [unit 0.5C]
 *  \note   Mxx\n - set mode to 0=manu 1=auto
 *
 *  \note   O - set to max temp (ventil open)
 *  \note   C - set to min temp /ventil closed)
