Who can resist a USB-Serial cable for less than $2? I couldn't, but then
found out that the cables I got didn't work with the ch341 linux driver. I 
think the cause of that is that I received a newer version of the CH341 chip
than the mainline driver was written for.

I snooped the USB traffic of the cable running in a windows VM using the windows
driver that came with the cables and figured out that the registers are mostly standard
16550 registers and was able to make my version of CH341 adapter work. Additionally, I
added parity support.
