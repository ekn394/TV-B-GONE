# AVRdude

## Installations
<li>Find and install winavr (as of this writing, this can be found at https://sourceforge.net/projects/winavr/ )</li>

<li>Install adafruit_drivers_2.0.0.0.exe which is included in this repo.</li>

## Connect your AVR programmer (in my case I am using the TinyISP AVR programmer from Adadruit 
https://www.adafruit.com/product/46

## Flashing the chip from Command Prompt 

<li>Navigate in CMD prompt to the directory of your tvbgone.hex file (in this example, I have it in c: drive) </li>
<li>Enter the following instruction </li>
<br>
avrdude -c usbtiny -p attiny85 -U flash:w:tvbgone.hex -U lfuse:w:0xfe:m -U hfuse:w:0xdf:m -U efuse:w:0xff:m

## Example

C:\>avrdude -c usbtiny -p attiny85 -U flash:w:tvbgone.hex -U lfuse:w:0xfe:m -U hfuse:w:0xdf:m -U efuse:w:0xff:m

avrdude: AVR device initialized and ready to accept instructions

Reading | ################################################## | 100% 0.02s

avrdude: Device signature = 0x1e930b
avrdude: NOTE: FLASH memory has been specified, an erase cycle will be performed
         To disable this feature, specify the -D option.
avrdude: erasing chip
avrdude: reading input file "tvbgone.hex"
avrdude: input file tvbgone.hex auto detected as Intel Hex
avrdude: writing flash (8164 bytes):

Writing | ################################################## | 100% 20.61s



avrdude: 8164 bytes of flash written
avrdude: verifying flash memory against tvbgone.hex:
avrdude: load data flash data from input file tvbgone.hex:
avrdude: input file tvbgone.hex auto detected as Intel Hex
avrdude: input file tvbgone.hex contains 8164 bytes
avrdude: reading on-chip flash data:

Reading | ################################################## | 100% 12.14s



avrdude: verifying ...
avrdude: 8164 bytes of flash verified
avrdude: reading input file "0xfe"
avrdude: writing lfuse (1 bytes):

Writing | ################################################## | 100% 0.02s

avrdude: 1 bytes of lfuse written
avrdude: verifying lfuse memory against 0xfe:
avrdude: load data lfuse data from input file 0xfe:
avrdude: input file 0xfe contains 1 bytes
avrdude: reading on-chip lfuse data:

Reading | ################################################## | 100% 0.02s

avrdude: verifying ...
avrdude: 1 bytes of lfuse verified
avrdude: reading input file "0xdf"
avrdude: writing hfuse (1 bytes):

Writing | ################################################## | 100% 0.00s

avrdude: 1 bytes of hfuse written
avrdude: verifying hfuse memory against 0xdf:
avrdude: load data hfuse data from input file 0xdf:
avrdude: input file 0xdf contains 1 bytes
avrdude: reading on-chip hfuse data:

Reading | ################################################## | 100% 0.00s

avrdude: verifying ...
avrdude: 1 bytes of hfuse verified
avrdude: reading input file "0xff"
avrdude: writing efuse (1 bytes):

Writing | ################################################## | 100% 0.02s

avrdude: 1 bytes of efuse written
avrdude: verifying efuse memory against 0xff:
avrdude: load data efuse data from input file 0xff:
avrdude: input file 0xff contains 1 bytes
avrdude: reading on-chip efuse data:

Reading | ################################################## | 100% 0.01s

avrdude: verifying ...
avrdude: 1 bytes of efuse verified

avrdude: safemode: Fuses OK

avrdude done.  Thank you.
