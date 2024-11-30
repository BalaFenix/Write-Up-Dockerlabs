<!DOCTYPE MD>

### Write Up Máquina Agua de Mayo DockerLabs

Descomprimimos archivo y desplegamos máquina

![alt text](assets/img1.png)

Realizo un escaneo de puertos con Nmap y busco posibles vulnerabilidades

![alt text](assets/img2.png)
![alt text](assets/img3.png)

Introduzco la IP en la URL del navegador seguido de **/images/** como me indicaba en el script de nmap y encuentro lo siguiente

![alt text](assets/img4.png)
![alt text](assets/img5.png)

Encuentro esta imagen miro sus metadatos con exiftool y no encuentro nada

![alt text](assets/img6.png)

Después descubro en el código lo siguiente:

![alt text](assets/img8.png)

Investigo y se trata de un código en Brainfuck, es un programa de programación esotérico que no conocía, para decodificarlo lo hago en línea a través de brainfuck interpreter

![alt text](assets/img9.png)

Es así como accedo mediante conexión ssh usando como usuario agua y como password bebeaguaqueessano, comienzo a escalar privilegios

![alt text](assets/img12.png)

Descubro que tenemos privilegios de root desde Bettercap, abro Bettercap como root e introduzco el comando: **!chmod +s /bin/bash** para activar el bit SUID a bash

![alt text](assets/img13.png)

Salgo de Bettercap e introduzco **/bin/bash -p** hago un whoami y ¡Ya somos root!

![alt text](assets/img14.png)
