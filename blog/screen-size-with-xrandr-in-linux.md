Extraído de [este post](https://rydzak.me/2020/08/kali-linux-adding-custom-resolution/)
Configurar monitor (screen) en linux.

`gtf` para obtener la configuración que buscamos y `xrandr` para cambiar la configuración. Esto es muy útil cuando se trabaja en una máquina virtual para hacer que ocupe la totalidad de la ventana.

```
➜ ~ gtf 3840 2160 60
3840x2160 @ 60.00 Hz (GTF) hsync: 134.10 kHz; pclk: 712.34 MHz
Modeline "3840x2160_60.00" 712.34 3840 4152 4576 5312 2160 2161 2164 2235 -HSync +Vsync

➜ ~ xrandr --newmode "3840x2160_60.00" 712.34 3840 4152 4576 5312 2160 2161 2164 2235 -HSync +Vsync

➜ ~ xrandr --addmode Virtual1 "3840x2160_60.00"

➜ ~ xrandr --output Virtual1 --mode "3840x2160_60.00"
```

