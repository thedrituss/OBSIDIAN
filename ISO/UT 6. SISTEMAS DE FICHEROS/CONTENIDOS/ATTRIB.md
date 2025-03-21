
Muestra, establece o quita los atributos de sólo lectura, modificado, sistema y oculto asignados a los archivos o a los directorios. Utilizado sin parámetros, __attrib__ muestra los atributos de todos los archivos del directorio actual.

###### SINTAXIS

```
attrib [{+r | -r}] [{+a | -a}] [{+s | -s}] [{+h | -h}] [[unidad:][rutaDeAcceso] nombreDeArchivo] [/s[/d]]
```

###### PARÁMETROS


``+r``
Establece el atributo de archivo de sólo lectura.

``-r``
Quita el atributo de archivo de sólo lectura.

``+a``
Establece el atributo de modificado (utilizado antiguamente para copias de seguridad, etc)

``-a``
Quita el atributo de modificado.

``+s``
Establece el atributo de archivo del sistema.

``-s``
Quita el atributo de archivo del sistema.

``+h``
Establece el atributo de archivo oculto.

`-h`
Quita el atributo de archivo oculto.

`Unidad: rutaDeAcceso nombreDeArchivo`
Especifica la ubicación y el nombre del directorio, archivo o conjunto de archivos de los que desea
mostrar o cambiar los atributos. En el parámetro ``nombreDeArchivo``, puede utilizar los caracteres
comodín (``?`` y ``*``) para mostrar o cambiar los atributos de un grupo de archivos.

``/s``
Aplica el comando ``attrib`` y las opciones de línea de comandos a los archivos coincidentes del
directorio actual y todos sus subdirectorios.

``/d``
Aplica el comando ``attrib`` y las opciones de línea de comandos a los directorios.

``/?``
Muestra Ayuda en el símbolo del sistema.