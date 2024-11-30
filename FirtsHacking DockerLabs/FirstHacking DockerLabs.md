<h1> Write Up de la Máquina FirstHacking de Dockerlabs</h1>

<img src="assets/1lkhfcqj.png" style="width:6.73472in;height:1.88319in" />

Este es mi primer WriteUp. Voy a iniciar con la máquina llamada Firsthacking nivel muy fácil de la plataforma Dockerlabs.

Para iniciarla me meto en la plataforma y descargo el archivo. Descomprimo el archivo y lo ejecuto en Kali con el comando **sudo bash auto_deploy.sh firsthacking.tar**
para iniciar el script que da paso a la máquina.
Despliego máquina y lo primero que voy a hacer es
un escaneo de puertos con nmap para ver qué puertos tiene abiertos y como poder acceder por alguno de ellos.

<img src="assets/0tpzb2dm.png" style="width:4.58403in;height:1.63333in" />

Descubro que sólo tiene abierto el puerto 21. Le hago un **nmap 172.17.0.2 -–script vuln** para ver qué vulnerabilidades puedo explotar.

<img src="assets/y0grstyp.png" style="width:6.93056in;height:3.39986in" />

Encuentro la vulnerabilidad **CVE-2011-2523** y la información que consigo sobre ella en incibe es la siguiente:
Descripción: vsftpd versión 2.3.4 descargado entre 20110630 y 20110703,
contiene una puerta trasera (backdoor) que abre un shell en el puerto
6200/tcp. Tiene una puntuación de 9,80/10 lo que la convierte en
crítica/alta.

Afecta a las siguientes versiones:

<img src="assets/4jdgxult.png" style="width:3.525in;height:1.41667in" />

Busco la vulnerabilidad y me indica que puedo explotarla en Metasploit

Inicio Metasploit, antes de buscar la vulnerabilidad creo un workspace
firtshacking.

<img src="assets/jro5dhaa.png" style="width:5.21667in;height:1.64167in" />
<img src="assets/1wndajak.png" style="width:2.66667in;height:1.5in" />
<img src="assets/rlycy1ls.png" style="width:6.8in;height:1.325in" />

Busco la vulnerabilidad en Metasploit

Selecciono el exploit y miro la información necesaria para explotarlo,
me solicita el RHOSTS el RPORT no es necesario ya que ya viene
configurado por el exploit.

<img src="assets/j5mox1vd.png" style="width:6.84167in;height:3.45in" />

<img src="assets/lotcfn4y.png"
style="width:5.90556in;height:1.35139in" />

¡Ya somos root!
