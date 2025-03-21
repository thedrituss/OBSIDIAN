##### [[Longitud de cabecera]]

- IP no tiene un tamaño de cabecera fijo
- Algunas opciones del protocolo añaden palabras de 32 bits
- Por eso se necesita saber dónde empiezan los datos en cada paquete

##### [[Código de redundancia]]

- El *checksum* se calcula (sin acarreo) de todas las palabras de 16 bits de la cabecera.
	- Excepto el propio *checksum*.
- Sirve para detectar errores de transmisión.
- Es adicional al que pueda tener la capa de transporte.

##### [[Identificación del paquete]] y *[[Fragment offset]]*

- Todos los paquetes IP tienen un identificador único: _identification_ y _fragment offset_
- Originalmente, un paquete se manda en un solo fragmento
    - Con _fragment offset_ a `0`
- Si se necesita dividir (MTU del nivel de enlace insuficiente)
    - Se parte en varios fragmentos
    - Cada uno de ellos indica el lugar de su primer byte de datos
- Cada fragmento puede volverse a dividir
- En el destino, se espera a que lleguen todos los fragmentos antes de enviarlo al protocolo de nivel superior

##### [[Flags]]

- El primero es para usos futuros.
- El segundo indica si este datagrama se puede fragmentar.
- El tercero dice si hay más fragmentos o es el último.
- El flag __DF__ (_don't fragment_) indica a los routers que no fragmenten el paquete si sobrepasa la __MTU__ (_maximum transfer unit_), sino descarta el paquete.

##### [[TTL (_time to live_)]]

- El enrutamiento IP puede tener problemas
    - Es posible que haya bucles en las rutas que hagan que un paquete de vueltas _por siempre_
- Para evitarlo, el paquete se descarta pasado un tiempo en segundos (originalmente)
    - Actualmente, el tiempo de vida se mide en saltos
- Generalmente, los paquetes se envían con TTL suficiente para atravesar Internet (64 o 255)

##### [[Protocolo de nivel superior]]

| Identificador | Protocolo                           |                                        |
| ------------- | ----------------------------------- | -------------------------------------- |
| 0x01          | ICMP                                | Internet Control Message Protocol      |
| 0x02          | IGMP                                | Internet Group Management Protocol     |
| 0x06          | TCP                                 | Transmission Control Protocol          |
| 0x11          | UDP                                 | User Datagram Protocol                 |
| 0x29          | IPv6                                | IPv6 Encapsulation                     |
| 0x59          | OSPF                                | Open Shortest Path First               |
| 0x73          | L2TP                                | Layer Two Tunneling Protocol Version 3 |
| 0x85          | FC                                  | Fibre Channel                          |
| 0x8F-0xFC     | UNASSIGNED                          |                                        |
| 0xFD-0xFE     | Use for experimentation and testing | RFC 3692                               |
| 0xFF          | Reserved for extra                  |                                        |

##### [[Dirección de origen y destino]]

- Son números de 32 bits
- Indican la dirección de origen y destino de IP
- Pueden no coincidir con la dirección de origen _real_
	- Por ejemplo, en los saltos intermedios
	- En esos casos, el origen y destino _en ese momento_ no son los indicados en la cabecera

