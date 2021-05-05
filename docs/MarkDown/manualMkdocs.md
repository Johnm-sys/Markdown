

## Lista de comandos para markDown  
___

1. mkdocs new nombre: siendo el "nombre" reemplazado por el nombre de nustro proyecto.  
    * Crea el archivo .yml: este contendra las variables de configuración
    * Crea una carpeta docs que contendra nuestros archivos de MarkDown
2. Generar codigo html apartir de archivos .md (extension de markdown), nos situamos en consola junto al archivo .yml y ejecutamos:   
```MarkDown 
mkdocs build
```
nos crea una carpeta "site" por defecto con el contenido en html para subir al repositorio
```MarkDown 
mkdocs build --clean
```
nos crea una carpeta limpiando la anterior, se ejecuta si ya teniamos una anteriormente  

3. Modo server: podremos visualizar cambios de nuestro contenido en vivo, para esto nos situamos en consola junto al archivo .yml, y ejecutamos:
```markdown y mkdocs
mkdocs serve
```
se genera un sitio web temporal y mkdocs quedara a la escucha, y cada vez que se modifiquen y guareden los cambios, la ventana del navegador se refrescara. Cerramos este modo con:
```bash
ctrl + c
```

4. Generar mas paginas con markdown: los nuevos archivos han de ser archivos de markdown, lo primero es definir estructura o organizacion de nuestros arhivos dentro de la carpeta "docs", ejemplo:
```dos
mkdocs.yml
docs/index.md
docs/capitulos/capitulo1.md
docs/capitulos/capitulo2.md
docs/anexos/anexo1.md
site/
```
estos archivos seconvertiran automaticamente, pero es necesario agregarlos a la barra de navegación, para esto agregamos los archivos al archivo .yml, ejemplo:
```yml
site_name: Mi proyecto
nav:
    - Inicio: index.md
    - Capítulo 1: capitulos/capitulo1.md
    - Capítulo 2: capitulos/capitulo2.md
    - Acerca de: acerca.md
    - Resumen de opciones: opc/opciones.md
```
Este codigo agregara un enlace para ser encontrado cuando generemos el codigo.
```yml
site_name: Mi proyecto
nav:
    - Inicio: index.md
    - Capítulos:
        - Capítulo 1: capitulos/capitulo1.md
        - Capítulo 2: capitulos/capitulo2.md
    - Acerca de: acerca.md
    - Resumen de opciones: opc/opciones.md
```
otro ejemplo, pero genera una opcion **desplegable**

5. pagina principal: MkDocs buscara un archivo con el nombre "index.md" ó "readme.md", de estos dos tiene priorida el index

6. Se puede escojer un tema: existen variedad de temas, el pordefecto es "mkdocs", pero se puede cambiar agregando theme en el .yml, y nos quedaria asi:
```yml
site_name: Mi proyecto
nav:
    - Inicio: index.md
    - Acerca de: acerca.md
    - Resumen de opciones: opciones.md
theme: mkdocs
```
aqui vemos el tema por defecto, pero mkdocs trae otro "readthedocs"

7. podemos tambien cambiar el favicon, agregando una carpeta "img" junto al archivo .yml, y agregamos nuetsra imagen con el nombre "favicon" de extencion .ico

8. mkdocs tiene una ayuda, ejecutando:
```mkdocs
mkdocs --help
```
no muestra los comandos de mkdocs
```mkdocs
mkdocs build --help
```
ayuda con un comando especifico, en este caso "build"

