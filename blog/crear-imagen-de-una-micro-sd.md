`# dd if=/dev/<device> status=progress | gzip > <image-name>.img.gz`
`# cat <image-name>.img.gz | gunzip | dd of=/dev/<device> status=progress`
