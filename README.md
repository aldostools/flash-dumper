# PS3 NAND/NOR/eMMC Flash/IDPS Dumper

[Dump NOR to USB](https://aldostools.github.io/flash-dumper/index_nor.html)<br>
[Dump NOR to HDD](https://aldostools.github.io/flash-dumper/index_nor_hdd.html)<br>
[Dump NAND to USB](https://aldostools.github.io/flash-dumper/index_nand.html)<br>
[Dump NAND to HDD](https://aldostools.github.io/flash-dumper/index_nand_hdd.html)<br>
[Dump IDPS to USB](https://aldostools.github.io/flash-dumper/index_idps.html)<br>
<br>

Official Thread:<br>
https://www.psx-place.com/threads/ps3xploit-idps-flash-dumpers.23123/

v410-492

* Added Support 4.86 HFW to 4.92 HFW (CEX)


v2.0.2

* Updated To Support 4.85 HFW


v2.0.1

* Updated To Support 4.84 HFW


v2.0

* Freeze issues - Fixed
* Occasional bad dumps - Fixed
* No beeps & shutdown. Replaced by a graceful ROP chain exit & return to browser. This gives the opportunity to the user to dump after patching & validate the dump with littlebalup's py checker. As long as the user does not shutdown/restart, it's still possible to recover from bad patching.
* Support for usb port 0,1,6 + sd/cf/ms cards.
* Multi firmware support on all dumpers (4.10+) & DEX support on 4.81.
* HDD editions for all dumpers & flash writer where a picture file placeholder is used for read/write operations.
* Javascript refactoring for performance & efficiency.
* ps3xploit.com will host the 2.0 update, no need for 3rd party sites.


v1.0 (Thanksgiving 2017 Release)

* Supports Direct OFW to CFW patching for All Phat and 2xxx Slim (minver 3.56 Dec 2010 and lower)
* the NOR/NAND writer will just copy 3Mb of CoreOS data to both ros0 & ros1 in the flash memory.
* There is only one version released for 4.82. The same hex patch file can be used on nor & nand.
* It's as safe as possible, with a check for usb device & patch file making the exploit hang instead of corrupting flash if file is not found.
* In case of corruption (extremely rare but could always happen), it's only a partial brick because no per console info ever gets erased so a hardware flasher could still be used if ever a recovery reboot was impossible
