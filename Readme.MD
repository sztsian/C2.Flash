Implement Silabs C2 flash programming protocol via NUCLEO-103RB, Arduino and EFM32ZG STK-3200 boards.
See https://www.silabs.com/Support%20Documents/TechnicalDocs/an127.pdf
and http://akb77.com/g/silabs/jump-to-silabs-step-1/ for details

Port AN127SW to NUCLEO-103RB
Add SendC2.exe command line utility to upload hex file to USB-DA
All timing tune for 72MHz CPU system clock.
Implement terminal mode for C8051 commands.
1.	C2CK	- PC8
2.	C2D		- PC9
	Use Morpho Headers to connect


1. Upload C2_Flash.pde sketch to Arduino
2. Start program C2.Flash.exe (need .NET 2.0)
    Target        Arduino        Atmel
      C2CK      - digital pin 5 (PortD 5)
      C2D       - digital pin 6 (PortD 6)
      GND       - GND


Port AN127SW to EFM32-STK3700
1. Connect
    Target        EFM32GG STK-3700
      C2D       - PC3
      C2CK      - PC0
      GND       - GND
