- _Classless Internet Domain Routing_
- La dirección IP ya no da información acerca de los bits reservados para la red y para host
- Las redes se identifican por la dirección de la red y el número de bits destinado a la misma.
	- 172.12.0.0/12
	- 192.18.0.0/15


#### [[Máscara de red]]

- Con CIDR las parte de la dirección red y host se calcula mediante las máscaras de red
- La máscara de red es un número binario:
	- Tantos 1's como el tamaño de la red CIDR
	- Los 0's necesarios para completar hasta los 32 bits
- Las máscaras de red también se expresan como 4 números decimales separados por puntos


#### [[Dirección de la red]]

- Con CIDR, la dirección de red sigue siendo la que tiene todos los bits del host a 0, y la de broadcast a 1.
- Sin embargo, ya no es tan fácil como con las clases
	- Los bits de la red no son múltiplos de 8
- Se utiliza una máscara de red, realizando la operación `AND` con la dirección IP para encontrar la dirección de red
- Ejemplo
	-  La dirección IP es 192.168.20.100/26
	-  La máscara de red son 26 1’s → 255.255.255.192
	-  La dirección pertenece a la red
			255.255.255.192
			AND 192.168.020.100
			-------------------
			192.168.020.064
	-  La red a la que pertenece es 192.168.20.64/26


#### [[Subnetting]]

- Consiste en crear subredes pequeñas dentro de una red de clase A, B o C
- Ejemplo
	> Conseguir 4 redes a partir de una red clase C
	   Hay que aumentar la máscara de red 2 bits (4 posibilidades)

|                | Redes             | Primer host    | Último host    | Broadcast      |
| -------------- | ----------------- | -------------- | -------------- | -------------- |
| Red original   | 192.168.20.0/26   | 192.168.20.1   | 192.168.20.62  | 192.168.20.63  |
| Primera subred | 192.168.20.64/26  | 192.168.20.65  | 192.168.20.126 | 192.168.20.127 |
| Tercera subred | 192.168.20.128/26 | 192.168.20.129 | 192.168.20.190 | 192.168.20.191 |
| Cuarta subred  | 192.168.20.192/26 | 192.168.20.193 | 192.168.20.254 | 192.168.20.255 |

###### Información
[Link 1](https://www.aprendaredes.com/calculadora-ip/)
[Link 2](https://arcadio.gq/calculadora-subredes-vlsm.html)


#### [[Supernetting]]

- A partir de varias redes pequeñas, conseguir una más grande
- Ejemplo
> Conseguir una red con más de 1000 hosts a partir de redes clase C