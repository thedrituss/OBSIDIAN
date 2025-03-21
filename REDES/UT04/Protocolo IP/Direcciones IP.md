
- Una dirección IP consta de 32 bits
- Por convenio, se representa como 4 números decimales, uno por cada byte.

| `192.168.1.1`                      |
| ---------------------------------- |
| `11000000101010000000000100000001` |

##### [[¿Qué identifican?]]

- Las direcciones no se asignan por host.
- Se asignan por interfaces del host
	- Un equipo con dos enlaces a la red tendrá dos direcciones IP
	- Los enlaces a la red pueden ser a la misma red o a redes distintas
- También un mismo interfaz puede tener más de una IP


##### [[Red y Host]]

- Las direcciones IP se asignan al montar la red, no como las MAC
    - Las direcciones MAC se asignan por el fabricante de la tarjeta, quedando distribuidas casi aleatoriamente
    - Las direcciones IP se estructuran de una forma jerárquica
- La dirección IP contiene dos partes
    - Una parte identifica a la red
    - Otra parte identifica al host/enlace dentro de la red

| 192.168.1.1 | Parte de red | Host |
| ----------- | ------------ | ---- |
|             | 192.168.1    | 1    |
|             | 192.168      | 1.1  |

