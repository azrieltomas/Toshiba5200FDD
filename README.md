# Toshiba 5200 FDD Adapter

This adapter converts the 26-way FDD IDC connector on the T5200 to a standard 34-way IDC connector. This way the old drive can be replaced with any 3.5" drive in case it fails (and by any, I mean any that only requires 5V).

Tested in:
* Toshiba T3200SX
* Toshiba T5200
	
Parts required:
* 26-way 2.54mm pitch IDC male header
* 34-way 2.54mm pitch IDC male header
* Corresponding 26-way and 34-way IDC cables
* 2-way header for jumper (& corresponding jumper pin)
* 4-pin Berg connector and two wires for the FDD power (you will need to solder this)

Due to limitations of the BIOS, the replacement drive can only format either 1.44MB or 720kB. This is defined by pin 9 on the 26-way (!NOTCH) connector. Inserting a jumper grounds this pin, setting it to 1.44MB, leaving it floating sets it to 720kB. Either way it will still read both kinds. Alternatively, you can format your floppies from DOS 3.3 or install a custom BIOS.

This also ties !READY to ground, which may cause issues if you have more than one drive installed.

With thanks to IanB on the Vogons forum. See his posts here: https://www.vogons.org/viewtopic.php?f=46&t=57998
