# "EtherWiz" Acorn Ethernet podule (WizNet W6100)

November 2025

A work in progress firmware for my Ethernet card using the WizNet W6100 device in MACRAW mode.  No 'legacy' components - everything is available as new/active hardware.   There's 512K flash on board rather than a podule ROM - the flash can be updated from RISC OS.

All RISC OS code (EtherWiz DCI4 Ethernet driver, podule binder, flashing code) is all my own work, written from scratch in BASIC assembler.   The ROM binder and flasher are still very crude quick implementations.

The driver works well enough to perform small file copies via ShareFS, then locks the machine and interrupts have not yet been implemented so this currently just polls at 100Hz.  DCI4 "Filtering" has not yet been implemented at all (all packets are forwarded to the Internet module) so this may be why the machine ultimately locks up.

## Licence

No warranty is provided, and this work is used at your own risk.  

Licenced as CC BY-SA 4.0

Copyright 2025 Ian Jeffray
