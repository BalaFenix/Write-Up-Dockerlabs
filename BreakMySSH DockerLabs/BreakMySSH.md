Descargamos la máquina de la plataforma DockerLabs, previamente debemos tener instalador dockers con el comando **_sudo_** **_apt_**
**_install_** **_Docker.io_**, descomprimimos los archivos y ejecutamos para desplegar la máquina.

<img src="assets/ym0swu13.png"
style="width:4.58333in;height:3.16667in" />

Vamos a realizar un escaneo de puertos con nmap

<img src="assets/v05d253r.png"
style="width:6.50667in;height:2.49583in" />

Veo que el único puerto abierto es el 22, el cual me permite establecer una conexión ssh, además la versión que utiliza tiene una vulnerabilidad de enumeración de usuarios conocido como CVE-2018-15473.

<img src="assets/511bdprk.png"
style="width:4.99375in;height:1.39153in" />

<img src="assets/uncur3ef.png" style="width:6.97917in;height:2.65in" />

Voy a utilizar metaspliot y este CVE para intentar averiguar el nombre de algún usuario para ello sigo los siguientes pasos:

<img src="assets/djnj03zx.png"
style="width:2.11389in;height:0.48611in" />

<img src="assets/iaux4tda.png"
style="width:6.9243in;height:1.78319in" />

<img src="assets/blaet1gd.png"
style="width:3.03236in;height:0.34722in" />

<img src="assets/3lyb01jn.png"
style="width:5.2075in;height:1.83472in" />

<img src="assets/2gf50ihb.png"
style="width:4.43333in;height:0.39167in" />

<img src="assets/ycxqimqo.png"
style="width:5.46389in;height:3.49139in" />

Una vez que he sacado el listado de usuarios de la máquina voy a hacer
fuerza bruta con hydra y un diccionario que previamente he descargado en
mi máquina.

La clave del usuario root es estrella
<img src="assets/rhd3s10z.png"
style="width:4.15708in;height:1.71319in" />

Establecemos la conexión ssh y accedemos a través de ella directamente a la máquina con privilegios
root.

<img src="assets/w4ayviq1.png"
style="width:3.22917in;height:2.89986in" />

¡Estamos dentro!
