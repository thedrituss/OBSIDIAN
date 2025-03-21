
###### [[MBR]]
- Sistema tradicional y mas extendido
- Soportado por todas las BIOS actuales
- Tamaño máximo de partición: __4TB__
- __MBR__ (Master Boot Record): primer sector (de arranque, __512 bytes__) del disco que guarda toda la información correspondiente a las posibles particiones del disco.
- ==4 Particiones __MÁXIMO__==
- 3 Particiones Primarias y 1 Extendida

###### [[GPT]]
- Estándar para la colocación de la tabla de particiones en un disco duro físico.
- Es parte del estándar Extensible Firmware Interface (EFI) propuesto por Intel para reemplazar la vieja BIOS del PC.
- Sistema más moderno, que pretende subsanar las deficiencias de MBR. Conserva MBR legacy por compatibilidad
- Tamaño máximo de particiones
	- Hasta 9,44 ZB (ZettaBytes) (1 ZB son 10 ^ 9 TB)
	- ==__128__ Particiones __máximo__==