<!DOCTYPE MD>

## Máquina Injection Dockerlabs.

Descomprimimos archivo y desplegamos la máquina
![alt text](img1.png)
Compruebo que hago ping con la máquina a la que voy a atacar
![alt text](img2.png)
Voy a realizar un escaneo de puertos y versiones a través de Nmap
![alt text](img3.png)
Busco vulnerabilidades con Nmap
![alt text](img4.png)
Introduzco el script que me ha indicado Nmap que es vulnerable en la URL del navegador e inyecto código
![alt text](img5.png)
![alt text](img6.png)
![alt text](img7.png)
Una vez que tengo el usuario y la clave voy a establecer una conexión SSH!
![alt text](img8.png)
Una vez que la tengo voy a ver si hay archivos mal configurados con el comando **find / -perm -4000 -type f 2>/dev/null** y voy a intentar ejecutar un shell de alguno de ellos
![alt text](img9.png)
pruebo a hacer la escalada de privilegios con todos los archivos hasta que puedo acceder con /usr/bin/env /bin/sh -p que lo utilizamos para decirle al archivo que no elimine los privilegios del SUID.
![alt text](img10.png)
¡Ya somos root!
