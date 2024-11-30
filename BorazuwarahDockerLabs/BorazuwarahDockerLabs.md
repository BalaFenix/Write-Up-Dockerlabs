<img src="assets/ylaklng5.png"
style="width:2.80833in;height:1.89167in" />

<img src="assets/2he4hate.png"
style="width:4.69167in;height:3.76667in" />

Como siempre para desplegar la máquina descomprimimos el archivo y lo ejecutamos con bash

<img src="assets/2z3w3woo.png"
style="width:4.54028in;height:1.24156in" />

Comprobamos que hacemos ping

<img src="assets/b4igyphq.png"
style="width:5.14958in;height:2.75903in" />
<img src="assets/vak52izu.png"
style="width:5.69931in;height:4.64167in" />

Realizamos escaner de puertos abiertos y del sistema operativo que tiene la máquina. Introducimos IP en la URL del buscador y nos encontramos la siguiente imagen.
Inspecciono el código pero no encuentro más que la imagen así que voy a probar con Gobuster a ver si
encuentro algún archivo más indexado a la página.

No encuentro nada así que paso a buscar en los metadatos de la imagen.

<img src="assets/agakeuf1.png"
style="width:5.40778in;height:4.08958in" />

<img src="assets/b1jiu4rm.png"
style="width:5.11944in;height:4.54972in" />

Para analizar los metadatos
de la imagen utilizo la herramienta exiftool, lo que encuentro en ellos
es que el usuario es borazuwarah.

<img src="assets/sbbkbpuw.png"
style="width:6.01389in;height:1.41653in" />
<img src="assets/llmt1d2i.png"
style="width:6.01361in;height:1.67361in" />
<img src="assets/5r2hrnjl.png"
style="width:6.04014in;height:2.4118in" />

Compruebo si se trata de un usuario con conexión SSH. Me descargo un diccionario para poder trabajar con Hydra.
Descubro la password del usuario con Hydra

<img src="assets/y404rmsl.png"
style="width:6.04847in;height:2.02708in" />Inicio conexión SSH

<img src="assets/qy4xjx22.png"
style="width:6.82083in;height:1.39167in" />
<img src="assets/nf1r11vk.png"
style="width:3.45833in;height:0.725in" />

Meto comando ls -l para ver a qué archivos tengo acceso, al no tener a
ninguno meto el comando sudo -l para ver quien tiene permisos de
superusuario

Introduzco sudo /bin/bash para abrir una nueva Shell de bash con
privilegios sudo

¡Ya somos root!
