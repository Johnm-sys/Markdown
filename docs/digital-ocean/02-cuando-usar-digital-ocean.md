# ¿Cuándo utilizar Digital Ocean?

Existen ciertos tipos de escenarios en donde, dependiendo del tráfico o de la cantidad de usuario, se necesitará cierta solución u otra.

* **Hosting gratis:** Cuando se despliega una aplicación en internet, se puede empezar con un Hosting gratuito, que sería la solución ideal si se tiene una decena de usuarios al día o al mes. Esta solución tiene una desventaja, que es que no permite acceder al hardware del servidor en donde está desplegada la aplicación, aparte de que es limitada y puede que aparezca publicidad.

* **Shared Hosting:** Esta solución brinda un poco más de hardware para desplegar aplicaciones, pero como en la solución anterior, también esta es limitada porque no permite administrar los recursos físicos del servidor y además que no permite instalar cualquier herramienta para correr las aplicaciones. Normalmente sólo cuenta con la arquitectura LAMP (Linux, Apache, MySQL y PHP).

* **VPS (Virtual Private Server):** Esta solución brinda una máquina virtual con recursos físicos administrables, y además, brinda la libertad de poder instalar cualquier herramienta para poder instalar la aplicación a desplegar. Esta solución es ideal cuando se tienen miles o decenas de miles de usuarios al mes.

* **Servidor dedicado:** Esta solución brinda una máquina física en donde todos sus recursos están dedicados sólo para la aplicación que se vaya a desplegar. Esta solución tiene una desventaja, y es que no se puede ampliar los recursos mientras el servidor está funcionando; es decir, es necesario apagarlo para poder ampliarlos. Esta solución es necesaria cuando se tienen decenas de miles o cientos de miles de usuarios al mes.

* **Cloud (Paas/Iaas):** Cuando la aplicación crece, se necesitará trabajar con una infraestructura, ya sea física o en la nube, en donde se tendrán servidores para balanceados de carga, servidores web, servidores de bases de datos, servidores de firewall; varios servicios para hacer funcionar la aplicación.

* **Datacenter:** En caso de tener millones de usuario o decenas de millones de usuarios al mes, es ideal tener esta solución, un propio datacenter.

Visto todo lo anterior, ¿cuándo es útil Digital Ocean? Digital Ocean es muy útil cuando se necesita una solución de tipo VPS, en donde se necesita administrar los recursos de hardware y se necesita ir creciendo a medida que avanza el proyecto. En este caso, Digital Ocean facilita mucho esta tarea.

Otras soluciones en la nube como AWS, Azure o Google Cloud Platform son más especializadas porque tienen una mayor cantidad de servicios, pero son más enfocadas a personas con el rol de DevOps (conocen más de infraestructura); mientras que Digital Ocean, es más enfocada a desarrolladores.