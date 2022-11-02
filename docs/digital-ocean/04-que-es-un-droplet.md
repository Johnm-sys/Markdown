# ¿Qué es un Droplet?

Droplet es la forma en la que Digital Ocean llama a sus servidores privados virtuales o VPS. Tienen la ventaja de utilizar discos de tipo SSD (estado sólido), que proporcionan tiempos de lectura y escritura más rápidos que los discos mecánicos giratorios convencionales.

## ¿Para qué sirve un Droplet?
Al igual que cualquier otro servidor privado virtual (VPS), un droplet es un sistema operativo virtualizado en un servidor remoto y es una de las formas en que se monta la infraestructura de Internet. Un VPS es una emulación de un servidor (por eso su nombre virtual) y proporciona un sistema operativo que se puede utilizar para administrarlo, usualmente siendo este una distribución de Linux o Windows server.

Este servidor virtual se emplea cuando se quiere proporcionar alojamiento a un sitio o aplicación web en Internet. También se utiliza cuando se quiere crear su propia plataforma de infraestructura en la nube o se pretende alojar software que necesita su propia instalación.

## ¿Cuáles son los beneficios de usar un droplet?
Los droplets son usados por Digital Ocean para ofrecer más flexibilidad, mejor desempeño y control que el hosting compartido que entregan otros proveedores de alojamiento web. El costo del hosting VPS es generalmente más alto que el del hosting compartido. Sin embargo, el VPS ofrece muchas ventajas.

La más importante es la posibilidad de personalizar el servidor para necesidades específicas y poder escalarlo de acuerdo a la necesidad. Además, Digital Ocean tiene la reputación de entregar servidores con un desempeño de primera, muy superior a otros competidores en factores como TTFB (Time to First Byte), entre otros.

## Pasos para crear primer droplets
* Buscamos la opcion de agregar o crear un droplet y damos click.
* Nos pide que seleccionemos la region, se recomienda asignar la más cercana a los usuarios que van a ingresar.
* Nos pedira unas opciones para selecionar lo que nos va a instalar.
    * Elegir una imagen, que es el sistema operativo que tendra. Nosotros elegimos (ubuntu-20.04 con una arquitectura de 64bits).
    * Maquina vistual en v¿conbinación de memoria y recursos, sugeridos para proyectos pequeños como aplicaciones, entorno de desarrollo/prueba. Nosotros seleccionamos la opcionde 7$/mes quue incluye 1 gb de ram, 25 gb de SSD, y transferencia de 1000gb).
    * Authentication se puede ingresar con una password enviada al correo cada vez que vayamos a ingresar o agregar nuestra clave ssh, nostros ya teniamos una clave SSH y la agregamos con el nombre "first-ssh-rsa".
    * Nos brinda mas opciones como copias de seguridad que se veran mas adelante.
    * Podemos iniciar mas de un droplet con esta configuración y el nos pregunta cuantos queremos.
    * Solo crearemos un Droplet y le asignaremos un nombre.
    * Se puede agregar etiquetas para ir encasillando su funcionamiento, nosotros le agregamos la etiqueta "educativo".
    * Ya podemos darle crear, y esperaremos a que digital ocean crea nuestro droplet.

Ingresar a nuestro droplet creado.

Para ello vamos a la consola y escribimos `ssh root@<ip>`, siendo **ip** la direccion dada por digital ocean, en nuestro caso la 159.223.155.217 

con `hostname` podemos ver el nombre del equipo en el que estamos, en el servidor al correr el comando nos brinda el nombre asignado al droplet.


