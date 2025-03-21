- IANA, por medio de RFC's, ha reservado varias redes para usos concretos.

| Red | Uso |
| --- |  --- |
| 127.0.0.0/8 | "loopback", utilizado para enviar paquetes IP al propio host |
| 10.0.0.0/8 | Red privada (RFC 1918) |
| 172.16.0.0/12 | Red privada (RFC 1918) |
| 192.168.0.0/16 | Red privada (RFC 1918) |
| 169.254.0.0/16 | Link Local o APIPA. Direcciones automáticas en redes pequeñas sin servidor DHCP |


#### Definición

- Una red privada (RFC 1918) son direcciones inválidas en Internet
	-  Un router de Internet descarta todos los paquetes con origen o destino en redes privadas
- Sirven para crear redes con IP que no forman parte de Internet
	-  Internas a organizaciones: Empresas, universidades, institutos. . .
- Objetivos:
-  No es posible ocultar direcciones de Internet: Ningún ordenador interno tendrá la dirección 8.8.8.8
-  Ahorro de direcciones IP
-  Siguen teniendo acceso limitado a Internet: NAT (se verá en otro tema)