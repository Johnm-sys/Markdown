

# Conceptos de HTML
## Indice
* [Concepto.](#conceptos)
* [Elementos.](#elementos)
* [Atributos.](#atributos)
* [Elementos de anidamiento.](#elementos-de-anidamiento)
* [Elementos vacíos.](#elementos-vacíos)
* [Anatomía de un documento HTML.](#anatomía-de-un-documento-HTML)
* [Imágenes.](#imágenes)
* [Marcando textos.](#marcando-textos)
* [Más información.](#más-información)
___
## Conceptos:
**HTML:** (Hyper Text Markup Language o lenguaje de marcado), se utitliza para estructurar una página web y su contenido.  

**Elemento:** Es un tipo de componente de HTML, tambien son las partes que componen los documentos HTML

---
## Elementos:
Anatomía de un Elemento: 

* Etiqueta de apertura: Consiste en el nombe del elemento envuelto entre paréntesis angulares (<>) de apertura y cierre, ejemplo:
```HTML
<p>
```
* Etiqueta de Cierre: Es la misma etiqueta que la de apertura, pero este incluye una barra inclinada (/) antes del nombre, ejemplo:
```HTML
</p>
```
* Contenido: es lo que va contenido entre la etiqueta de cierre y apertura, ejemplo:
```HTML
<p> this is the content </p>
```  
---
## Atributos
Los atributos contienen información adicional que no se desea que aparezca en el elemento, ejemplo:
```HTML
<p class="editor__note">My cat is very beautifull</p>
```
Donde 'class' es el nombre del atributo y 'editor__note' es el valor del atributo.  
características del atributo:  

* Debe tener un espacio antes del escribir el atributo.
* En nombre del atributo seguido de un igual(=).
* El valor del atributo envuelto por comillas de apertura y cierre.  
  
---
## Elementos de anidamiento:
Se puede colocar un elemento dentro de otro elemento, esto es conocido como anidamiento, ejemplo:
```HTML
<p>My cat is <strong>very</strong> grumpy.</p>
```
es necesario asegurarse de cerrar bien los elementos, primero se debe cerrar el elemento 'strong' debido a que esta interno y ya despues se cierra el elemento externo.  

---
## Elementos vacíos:
Algunos elementos no tienen contenido y se denominan elementos vacíos, ejemplo:
```HTML
<img src="images/firefox-icon.png" alt="My test image">
```
Este elemento contiene atributos pero no tiene una etiqueta de cierre (`</img>`)

---
## Anatomía de un documento HTML:
Html tiene una estructura por defecto:
```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>My test page</title>
  </head>
  <body>
    <img src="images/firefox-icon.png" alt="My test image">
  </body>
</html>
```
* `<!DOCTYPE html>`: Hoy en día no hace mucho, pero nos sirve para asegurarnos de que el documento se comporte correctamente.
* `<html></html>`: Usualmente conocido como elemento raiz, y este envuelve todo el documento.
* `<head></head>`: Elemento que funciona como contenedor para incluir material dentro del documento html, este contenido no es mostrado a los visitantes de la página.
* `<meta charset="utf-8">`: Elemento establece un conjunto de caracteres de la gran mayoria de los idiomas escritos.
* `<title></title>`: Establece el título de la página, este título aparece en la pestaña del navegador.
* `<body></body>`: Este contiene todo el contenido que desea mostrar a los usuarios web cuando visitan su página.   

---
## Imágenes:
Incrusta una imagen en nuestra página en la posición en la que aparece, ejemplo:  
```html
<img src="images/firefox-icon.png" alt="My test image">
```  
* ***src***: Contiene la ruta de la imagen ya sea local (como en el ejemplo) ó una link web.
* ***alt***: Contiene la descripción de la imagen en caso de que ocurra algun error.  

---
## Marcando textos:
1. Encabezados:
    * #### Mi subtítulo secundario => `<h4>Mi subtítulo secundario</h4>`
    * ### Mi subtítulo => `<h3>Mi subtítulo</h3>`
    * ## Mi título de nivel superior => `<h2>Mi título de nivel superior</h2>`
    * # Mi título principal => `<h1>Mi título principal</h1>` 

2. Párrafos: 
    * Estos elementos son para contener párrafos de texto => `<p> Mi párrafo </p>`  
  
3. Listas:
    Existen dos tipos de listas, pero funcionan de manera similar.
    * ***Listas desordenandas:*** estas listas se caracterizan por contar con viñetas (*) para separar cada item, pero este elemento debe contener cada item, y su código es:   
    `<ul>items</ul>`
    * ***Listas ordenandas:*** estas listas se caracterizan por contar con números seguido de un punto (1.) para separar cada item, pero este elemento debe contener cada item, y su código es:  
    `<ol>items</ol>`
    * ***Elemento de listas:*** Cada elemento dentro de una lista se coloca rodeado por:  
    `<li>Elemento Lista</li>`   
Ejemplo lista desordenada:  

```html
<ul>
    <li>Item 1</li>
    <li>Item 2</li>
</ul>
```
> Resultado:

> * Item 1  
> * Item 2

* Ejemplo lista ordenada:
```html
<ol>
    <li>Item 1</li>
    <li>Item 2</li>
</ol>
```
> Resultado:

> 1. Item 1
> 2. Item 2


4. Enlaces: Son elementos importates que al dar click nos llevaran en la web a un lugar específico que nostros marquenos, su código es:
```html
<a href="https://www.google.com">Ir a google</a>
```
* Contenido: es el texto que dira el enlace
* href: es el nombre del atributo y su valor contendra la dirección web a la que nos llevará el enlace.

> Resultado:   
> [Ir a google](https://www.google.com)   

----
## Más información

> * Para más información ir a [developer.mozilla.org](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/HTML_basics).
> * La información suminstrada es solo un resumen personal, esta es sacada y pertenece a [developer.mozilla.org](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/HTML_basics). 

[Volver Arriba ↑](#Conceptos-de-HTML)