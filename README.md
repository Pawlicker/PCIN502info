# PCIN502info
NEC PC-IN502, information and RS-232 dumps

# Background

From 1985 to around 1990, NEC manufactured the PC-IN502, a scanner designed for NEC’s PC-9801 and 8801 microcomputers. The scanner was very primitive, only being able to scan black and white images. Unfortunately, as anyone with old computers knows, many vintage scanners ended up discarded due to being obsoleted and taking up a lot of room. After all, what’s the purpose in using a 1985 era black and white scanner in 2024? Even later on in the lifespan of Japanese computers, many artists began to move to nicer scanners such as the Epson GT-6000, 8000, and 6500 that could do fancy features like color.

Well, there’s a good reason. The PC-IN502 was supported by many PC-9801, 8801, and even at least one Sharp X68000 drawing program. Before cheap drawing tablets and later many pen enabled Windows/Android/iOS tabs were the craze, the method of digitizing your images included using a scanner to scan in your image. This was depicted in the manga 16-bit Sensation, which had a very loose anime adaptation made recently that deviated extremely from the source material (but made people outside Japan learn what a PC-98 is). Also, PC-98 flatbed scanners tend to show up rarely on auction sites and I just so happened to get one, and it was a PC-IN502.

# Some basic information

The NEC PC-IN502 has both a serial and parallel port, however nearly all software uses the serial port. There are some serial settings to change the bitrate, which is mostly assumed to be 9600 8n1 for most software (and this is what I used). You do in fact need a null modem cable/dongle and not a straight through cable, or else you’ll get nothing out of your scanner. This is unsurprising, I found out that serial printers and other serial adapters do as well when researching why mine didn’t seem to work.

The scanner bulb is an off the shelf florescent bulb (NEC FL8W) and was engineered to be replaceable, and a side panel allows replacement easily. There’s also a grid overlay that came with the scanner, I’m not sure what the purpose of it was but it was used for something.

Multiple programs including Multi Paint System and Z’s Staff KID98 supported this on the PC-98, while the x68000 supports this as well on the PC-8801. On the X68000, Z’s Staff PRO-68k works with this scanner as well. JEDAI does not support this, but IIRC it supports reading/writing of MAG files so I’m sure you can scan with the other tools and import it. 

There are several resolution options, but when you increase the resolution, it scans less of the paper as it fills up the 640x400 buffer faster. When the scanner turns on, it lights the bulb for a few seconds, before doing a quick motor check and turning off the bulb.

# Source code to communicate with it

One program designed to communicate with the PC-IN502 back in the day was preserved by its author. This was written in ASM and provides commented (in Japanese) source code.

http://mzisland.com/club/in502/index.html

http://mzisland.com/club/in502/list.html

# Dumping serial packets

Due to the obscurity of the scanner and to help preservation efforts, I have dumped serial packets using NP21w and Windows 10 on a HP ProBook 6560b (with the onboard serial port), and the Free Serial Analyzer (freeserialanalyzer.com) in the trial mode. Why? I wanted to get this thing preserved for other Japanese computing enthusiasts. 

I made several scans using KID98, as MPS was unable to detect the scanner. This might be due to an emulation bug, or an incompatibility with MS-DOS 5.00A-H, which I used as it did work with other scanning tools. However, it did scan, and I was able to do multiple scans with different settings and then a few at the default 90dpi 400 line setting at the end. 

