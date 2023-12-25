# Buying a RISC V SBC
I recently bought a [Mango Pi MQ-Pro](https://github.com/mangopi-sbc/MQ-Pro). 
![](assets/mangopi.png)
This Single Board Computer (SBC) has the same factor form of a Raspberry Pi Zero, but uses RISC V's ISA is built with the D1 System on a Chip (SoC). 

## Searching for information
The first thing i did when i got it was to start looking for what to do with it and learn something interesting in the process. So i started searching for information in the internet and suddenly i was faced with a lot of documentation and information on the Mango Pi MQ-Pro. Some were:
- [sunxi's wiki entry](https://linux-sunxi.org/MangoPi_MQ-Pro)
- [boosterl's awesome-mango-pi-mq-pro repository](https://github.com/boosterl/awesome-mango-pi-mq-pro)

## How to communicate with the board and operating system
With this new information i tryed to find a way to communicate to the SBC. At first i tryed with [xfel](https://github.com/xboot/xfel) but i found it really painful because it seems that i didnt want to read/write such a low level data/instructions to RAM or ROM, because i dont understand it that good (i was able to write information to turn on and off a LED though). 
![](assets/mangopi-led.png)
So i opted to use UART and got a 3.3V UART to USB adapter and soldered it to the I/O pins as usual.
![](assets/mangopi-uart.png)

Then i figured out that for getting any UART information through the adapter i needed somoething to generate that information. I wondered what if i wrote that information but suddenly (fake, took me some time) realized that i wasnt going to waste my time on writing my own OS, so i downloaded images of various OS, hopped through them distros and finaly found that the best one for this was [arch linux](https://archriscv.felixc.at/) (as usual).

Now, with UART, i was able to look at what was happening inside the SBC in a low level but not that low as pure binary. This plus the Arch Linux installation, enabled me to get a terminal and configure the wifi and other stuff.

### Build, configure, upload, configure
Nowadays im using sehraf's [d1-riscv-arch-image-builder](https://github.com/sehraf/d1-riscv-arch-image-builder) bash scripts for building and uploading to the micro sd card. I've modified it to my needs such that i dont need to configure the OS through getting a terminal with UART, but it configures all what i need, including an ssh server for me to connect through my network.
