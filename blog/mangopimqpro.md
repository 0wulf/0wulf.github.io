# Mango Pi MQ-Pro
## Buying a RISC V SBC
I recently bought a [Mango Pi MQ-Pro](https://github.com/mangopi-sbc/MQ-Pro).


<img src="assets/mangopi.png" width="600"/> 



This Single Board Computer (SBC) has the same form factor of a Raspberry Pi Zero, but uses RISC V's ISA and is built with the [Allwinner D1](https://linux-sunxi.org/D1) System on a Chip (SoC). 

## Searching for information
The first thing I did when I got it was to start looking for what to do with it and learn something interesting in the process. So, I began searching for information on the internet and suddenly was faced with a lot of documentation and information on the Mango Pi MQ-Pro. Some sources included:
- [sunxi's wiki entry](https://linux-sunxi.org/MangoPi_MQ-Pro)
- [boosterl's awesome-mango-pi-mq-pro repository](https://github.com/boosterl/awesome-mango-pi-mq-pro)

## How to communicate with the board and operating system
With this new information, I tried to find a way to communicate with the SBC. Initially, I tried with [xfel](https://github.com/xboot/xfel)  but found it painful because it seemed that I didn't want to read/write such low-level data/instructions to RAM or ROM, as I don't understand it that well (although I was able to write information to turn on and off an LED).
<img src="assets/mangopi-led.png" width="600"/> 


I opted to use UART and got a 3.3V UART to USB adapter, soldering it to the I/O pins as usual.
<img src="assets/mangopi-uart.png" width="600"/> 


Then, I figured out that to get any UART information through the adapter, I needed something to generate that information. I wondered what if I wrote that information, but suddenly (fake, took me some time) realized that I wasn't going to waste my time writing my own OS, so I downloaded images of various OS, hopped through them distros, and finally found that the best one for this was [Arch Linux](https://archriscv.felixc.at/) (as usual).

Now, with UART, I was able to look at what was happening inside the SBC at a low level but not as low as pure binary. This, plus the Arch Linux installation, enabled me to get a terminal and configure the WiFi and other stuff.

### Build, configure, upload, configure
Nowadays, I'm using sehraf’s [d1-riscv-arch-image-builder](https://github.com/sehraf/d1-riscv-arch-image-builder) bash scripts for building and uploading to the micro SD card. I’ve modified it to my needs so that I don't need to configure the OS through getting a terminal with UART, but it configures all I need, including an SSH server for me to connect through my network.
