<!DOCTYPE MD>

### Write Up Máquina Agua de Mayo DockerLabs

Descomprimimos archivo y desplegamos máquina

![alt text](img1.png)

Realizo un escaneo de puertos con Nmap y busco posibles vulnerabilidades

![alt text](img2.png)
![alt text](img3.png)
Introduzco la IP en la URL del navegador seguido de **/images/** como me indicaba en el script de nmap y encuentro lo siguiente

![alt text](img4.png)
![alt text](img5.png)
Encuentro esta imagen miro sus metadatos con exiftool y no encuentro nada

![alt text](img6.png)
después descubro en el código lo siguiente:

![alt text](img8.png)
investigo y se trata de un código en Brainfuck, es un programa de programación esotérico que no conocía, para decodificarlo lo hago en línea a través de brainfuck interpreter

![alt text](img9.png)
es así como accedo mediante conexión ssh usando como usuario agua y como password bebeaguaqueessano, comienzo a escalar privilegios

![alt text](img12.png)
Descubro que tenemos privilegios de root desde Bettercap, abro Bettercap como root e introduzco el comando: **!chmod +s /bin/bash** para activar el bit SUID a bash

![alt text](img13.png)
Salgo de Bettercap e introduzco **/bin/bash -p** hago un whoami y ¡Ya somos root!

![alt text](img14.png)
