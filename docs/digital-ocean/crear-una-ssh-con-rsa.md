
# Crear una clave SSH 

* Nosotros tenemos windos pero funciona mas o menos parecido para este paso a paso usaremos la consola de bash.
* en la consola nos dirigimos a la ruta raiz con `cd` nos llevara a la ruta raiz o ~.
* Desde raiz buscaremos el directorio ".ssh", si este no existe lo creamos corriendo `mkdir .ssh`.
* Ingresamos al directorio con `cd .ssh`.
* Alli crearemos un clave corriendo `ssh-keygen -t rsa` con los paremetros de rsa para que sea de este tipo
* Nos pedira un nombre pero damos enter para que nos deje el default.
* Nos pedira una contraseña que nos pida cada vez que vamos a ingresar a los servidores, luego volvemos a dar enter.
* y nos genera la clave Rsa.
* vemos los archivos que nos genero, son dos arhicos con el mismo nombre "id_rsa" uno publico y otro privado.
* Vemos la data del archivo publico con `cat id_rsa.pub` en consola y nos muestra el contenido de la llave.
* copiamos el contenido para llevarlo a donde necesitemos.


### agregar el path del la llave ssh privada

No esta probada
`
ssh -i /path/to/your/private_ssh user@ip
`