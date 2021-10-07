# INSTALACIÓN DE UNA MÁQUINA VIRTUAL Y JAVA
## 1. Instalación de una máquina virtual y sistema operativo

Una máquina virtual es, en esencia, un software encargado de emular, en este caso, un ordenador. Además, como cualquier computadora, esta va a contar con un sistema operativo, disco duro, memoria ram, entre otros pero de manera virtual (el usuario es quien va a determinar todos estos aspectos a través del software y vendrá limitado por las características del propio ordenador que esté ejecutando la máquina virtual).

Así pues, a continuación se explicará, grosso modo, la instalación de una máquina virtual así como de el Sistema Operativo (SO) necesario para su funcionamiento

En primer lugar se deberá de descargar el programa VirtualBox (la versión más actual, en este caso será la 6.1) desde la página oficial de Oracle VM VirtualBOX.

![Figura.1.Página de descarga de VirtualBox. [Elaboración propia]](https://raw.githubusercontent.com/jdabrante/INFORME-N-1/DAW/1.png "Figura.1.Página de descarga de VirtualBox. [Elaboración propia]") 

Una vez instalado el programa en el ordenador se procederá a la creación de la máquina virtual con el  Sistema Operativo (SO) correspondiente (en este caso Ubuntu 20 como bien se muestra en la figura 2).

![Figura.2.Página de descarga de Ubuntu 20. [Elaboración propia]](https://raw.githubusercontent.com/jdabrante/INFORME-N-1/DAW/2.png "Figura.2.Página de descarga de Ubuntu 20. [Elaboración propia]")

El siguiente paso será definir la cantidad de memoria (RAM) que será reservada para la máquina virtual (esto dependerá del equipo que estemos utilizando, en este caso se utilizarán 4000 MB ya que se disponen de 16384 MB, teniendo en cuenta pues que el valor que se dé a la memoria reservada nunca podrá ser superior o igual al la del propio equipo), así como también el espacio disponible que tendremos en la misma (el almacenamiento seguirá el mismo principio la memoria ram).
Una vez finalizado este proceso, el siguiente paso será iniciar la máquina virtual y seleccionar el archivo (disco óptico virtual de Ubuntu 20) que hemos descargado previamente de internet (Fig.4). 

![Figura.4. Ventana de VirtualBox donde se muestra el archivo del disco duro óptico virtual de Ubuntu 20. [Elaboración propia]](https://raw.githubusercontent.com/jdabrante/INFORME-N-1/DAW/3.png "[Figura.4. Ventana de VirtualBox donde se muestra el archivo del disco duro óptico virtual de Ubuntu 20. [Elaboración propia]")

Así pues una vez terminado este paso comenzaría la instalación del SO, ya estaría todo preparado para empezar a utilizar la máquina virtual.

## 2.Instalación de Java en el SO

Una vez creada la máquina virtual, a continuación será necesaria la instalación de diversos softwares dentro de la misma que nos permita compilar e interpretar un lenguaje de programación como Java. Para ello, en este caso se instalará Java a través de OpenJDK. Para ello habrá que seguir los pasos que se detallaran con los siguientes puntos.

### 2.1 Instalación de Java en Ubuntu desde el repositorio
Para ello se abrirá el terminal desde dentro de la máquina virtual a través del conjunto de teclas CTRL+ALT+T.
Una vez abierto el terminal se procederá a actualizar el sistema a través del comando (Fig.5):

**<p align="center"> sudo apt-get update </p>**

Una vez introducido el comando se iniciará la actualización como bien se muestra en la figura 6.

![Figura.5.Ventana del terminal con el comando correspondiente para la actualización del sistema. [Elaboración propia]](https://raw.githubusercontent.com/jdabrante/INFORME-N-1/DAW/4..png "Figura.5.Ventana del terminal con el comando correspondiente para la actualización del sistema. [Elaboración propia]")

![Figura.6. Actualización del sistema completado a través del terminal.[Elaboración propia]
](https://raw.githubusercontent.com/jdabrante/INFORME-N-1/DAW/5..png "Figura.6. Actualización del sistema completado a través del terminal.[Elaboración propia]")

Terminada la actualización, se podrá proceder a la instalación de Java a través del JDK. Para ello se utilizará el comando (Fig.7):


**<p align="center"> sudo apt-get install default-jdk  </p>**


![Figura.7. Ventana del terminal con comando para instalar Java por defecto.[Elaboración propia]
](https://raw.githubusercontent.com/jdabrante/INFORME-N-1/DAW/default-jdk.png "Figura.7. Ventana del terminal con comando para instalar Java por defecto.[Elaboración propia]")

![Figura.8. Ventana del terminal donde se refleja la instalación completa de Java.[Elaboración propia]](https://raw.githubusercontent.com/jdabrante/INFORME-N-1/DAW/6..png "Figura.8. Ventana del terminal donde se refleja la instalación completa de Java.[Elaboración propia]")

Una vez hecho esto se habrá instalado la versión por defecto de java, es decir, la última versión. Esto se podrá comprobar con el siguiente comando (Fig. 9), observando así además en la siguiente figura que la última en ese caso es la 11.0.11:

![Figura.9. Ventana del terminal con comando para comprobar la versión de java.[Elaboración propia].
](https://raw.githubusercontent.com/jdabrante/INFORME-N-1/DAW/java-version.png "Figura.9. Ventana del terminal con comando para comprobar la versión de java.[Elaboración propia]")

Hay que tener en cuenta el hecho de que algunos comandos  pedirán la contraseña del usuario, por lo que es muy importante recordar esta.

### 2.2 Instalación de una versión específica de Java

Una vez instalado Java y comprobada la versión (11.0.11 en este caso), será necesario conocer cómo instalar otras versiones del mismo. Para ello se utilizará el comando:

**<p align="center"> sudo apt install openjdk-*-jdk </p>**

Donde “*” será la versión que se quiera instalar.

En este caso se instalará la versión 11, seguida de la 9 y por último la 8 (esta última será la que en este caso en concreto se dejará instalada).
Así pues en las siguientes imágenes se recoge cada una de las instalaciones.

![Figura.10.Instalación de Java 11. [Elaboración propia]](https://raw.githubusercontent.com/jdabrante/INFORME-N-1/DAW/7..png "Figura.10.Instalación de Java 11. [Elaboración propia]")

![Figura.11. Instalación de Java 9.[Elaboración propia]](https://raw.githubusercontent.com/jdabrante/INFORME-N-1/DAW/8..png "Figura.12. Instalación de Java 8.[Elaboración propia]")

![Figura.12. Instalación de Java 8.[Elaboración propia]](https://raw.githubusercontent.com/jdabrante/INFORME-N-1/DAW/9..png "Figura.12. Instalación de Java 8.[Elaboración propia]")

Se puede apreciar como en la instalación de Java 9 se produce un error (se resalta con una “E” roja en la figura 11). Esto es debido a que ya no presenta soporte esta versión.

No obstante, aunque se ha instalado correctamente la versión 8 de Java, al introducir el comando java --version , seguirá apareciendo la versión 11 como bien se observa en la siguiente imagen.

![Figura.13. Ventana donde se muestra la versión de Java 11 aún habiendo instalado Java 8.[Elaboración propia]
](https://raw.githubusercontent.com/jdabrante/INFORME-N-1/DAW/10..png "Figura.13. Ventana donde se muestra la versión de Java 11 aún habiendo instalado Java 8.[Elaboración propia]")

La resolución de este problema se hará en el siguiente punto.

### 2.3 Configuración de las variables de entorno

A continuación se deberán de actualizar las variables de entorno. Para ello en primer lugar será necesario conocer qué versiones de OpenJDK se han descargado en el sistema, esto se podrá conocer utilizando el comando:

**<p align="center"> ls /usr/lib/jvm </p>**

![Figura.14. Ventana del terminal donde se reflejan las versiones de OpenJDK disponibles
 en el sistema.[Elaboración propia]](https://raw.githubusercontent.com/jdabrante/INFORME-N-1/DAW/11..png "Figura.14. Ventana del terminal donde se reflejan las versiones de OpenJDK disponibles en el sistema.[Elaboración propia]")
 
 Así pues, para elegir la versión que se desea se podrá utilizar el comando:

**<p align="center"> sudo update-alternatives --config java </p>**

![Figura.15. Opciones de versión de OpenJDK.[Elaboración propia]](https://raw.githubusercontent.com/jdabrante/INFORME-N-1/DAW/12..png "Figura.15. Opciones de versión de OpenJDK.[Elaboración propia]")

Por último se selecciona el valor correspondiente a la versión y se comprueba con el comando java --version.

![Figura.16. Elección de la versión de OpenJDK y comprobación de la versión instalada.[Elaboración propia]
](https://raw.githubusercontent.com/jdabrante/INFORME-N-1/DAW/13..png "Figura.16. Elección de la versión de OpenJDK y comprobación de la versión instalada.[Elaboración propia]")

Una vez terminado todos los pasos ya estará pues instalado Java en la versión que se desee utilizar.



 
 

