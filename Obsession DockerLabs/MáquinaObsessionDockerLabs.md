<!DOCTYPE md>

## Writte Up Máquina Obsession DockerLabs.

Para desplegar nuestra máquina que previamente hemos descargado de la plataforma DokerLabs tenemos que descomprimir el archivo con **unzip obsession.zip** Lo ejecutamos y desplegamos la máquina

![alt text](assets/image.png)

Compruebo que tengo conexión con la máquina haciendo ping

![alt text](assets/image-1.png)

Realizo escaneo de puertos y versiones con Nmap

![alt text](assets/image-2.png)

Busco alguna vulnerabilidad con **nmap --script vuln**

![alt text](assets/image-5.png)

Introduzco la IP de la máquina /backup como se me indicaba en el escaneo anterior y encuentro un archivo .txt

![alt text](assets/image-6.png)

![alt text](assets/image-7.png)

Trabajo con hydra y el diccionario rockyou.txt para sacar la password del usuario russoski

![alt text](assets/image-8.png)

Intento iniciar conexión SSH pero me aparece el siguiente mensaje, así que cambio la clave del servidor para conseguir el acceso por SSH

![alt text](assets/image-13.png)
![alt text](assets/image-14.png)

Utilizo el comando sudo -l para ver qué tiene usuarios root y como puedo escalar privilegios

![alt text](assets/image-15.png)

Veo que puedo hacerlo a través de Vim y consulto en https://gtfobins.github.io/ introduzco el comando **sudo vim -c ':!/bin/sh'** y...!ya somos root!

![alt text](assets/image-16.png)
