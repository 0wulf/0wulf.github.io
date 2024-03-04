# Utilizando gzip y gunzip
## De la SD a la imagen comprimida
`# dd if=/dev/<device> status=progress | gzip > <image-name>.img.gz`

## De la imagen a la SD
`# cat <image-name>.img.gz | gunzip | dd of=/dev/<device> status=progress`

# Utilizando XZ Utils
## Nota
Si el archive que se busca generar va a ser muy grande es buena idea utilizar xz
