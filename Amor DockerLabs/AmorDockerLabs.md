**Write Up Maquina Amor de DockerLabs**

Descargamos la máquina y descomprimimos con el comando **Unzip** desplegamos máquina con **sudo bash auto_deploy.sh amor.tar**

Una vez que compruebo que he hecho ping a la IP de la máquina 172.17.0.2 inicio un mapeo con Nmap y el comando **nmap 172.17.0.2 -p- -sV** para conocer los puertos que tiene abiertos y las versiones que utiliza.

![alt text](assets/img1.png)

Meto la IP en la URL y encuentro lo siguiente:

![alt text](assets/img2.png)

Creo una lista con dos usuarios : Juan y Carlota y trabajo con el comando de hydra **hydra -L listamor.txt -P rockyou.txt ssh://172.17.0.2** para hacer fuerza bruta e intentar sacar las credenciales de alguno de los dos usuarios que aparecen en la página.
