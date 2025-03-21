

## [[WINDOWS]]

```
chkdsk d:
	(chequea, informa pero no repara)

chkdsk d: /f
	(chequea e intenta reparar)

chkdsk c: /r
	(chequea también sectores defectuosos)

chkdsk c: /r /scan /perf
	(chequea y optimiza para rendimiento)
```


## [[LINUX]]

El comando __fsck__ hay que realizarlo con el file system desmontado.

```
lsblk -f 
umount /dev/sda6


fsck /dev/sda6
	(chequea y corrige preguntando al usuario antes)

fsck -y /dev/sda6
	(chequea y corrige sin preguntar)

fsck /dev/sda6 -f
	(fuerza el chequeo aunque el file system esté limpio)
```
