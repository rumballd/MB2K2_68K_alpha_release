# MB2K2_68K_alpha-release - note: not complete!
The MB2K2 was designed to be more than just an emulator for the 6809 and this is a new project to expand its capabilities.

In the mid ‘80s there was a follow on to the Microbox 2 called (with stunning originality) the Microbox 3. This was based around the Motorola 68000 CPU and matching RMS (Raster Management System), some details of this can be found on GitHub in the Microbox Archive (https://github.com/rumballd/Microbox-Archive/tree/master/MB3).

Sadly just as the MB3 was due to be launched, Motorola cancelled the RMS chipset and so the MB3 became the computer that never was. However the development work was almost complete so the sources for the system monitor (MONK) and several OS ports exist.

This the initial version of the firmware to run a Microbox 3 emulation on the MB2K2 board. It has a more of less complete memory map with 256KB of system RAM and various other non contiguous pieces of RAM and ROM to allow the original’s software to (theoretically) run unmodified.

There is a partial emulation of the RMS chips together with functional RTC, PIA and dual ACIAs. Keyboard input can be either via ACIA (USB) or PIA (PS/2 interface) and text out either ACIA or a bitmapped terminal emulation on the VGA display (640x480) as per the original.

Still to go are the mass storage drivers for the PROMdisk and non volatile RAMdisk and then an OS port.

If you have an XTAG interface download this and try it out on your MB2K2.

Details on flashing the MB2K2 are in the documentation but note that this will erase your current PROMdisk so if you have added any additional files to it please be sure to save these before loading the new binary image.

Use the Xmos command line and type :-
xflash -—verbose -—no-compression mb2k2_68k_release_usb.xe
Just use the instructions in the construction guide to restore your MB2K2 afterwards.



