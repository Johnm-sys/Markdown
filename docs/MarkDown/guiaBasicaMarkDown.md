<!-- Heading -->
# MarkDowm
---
## Indice  

* [Conceptos](#conceptos)
* [Qué es Markdown](#que-es-markdown)
* [Encabezado](#encabezado)  
* [Enfatizar](#enfatizar)  
* [Listas](#listas)  
* [Enlaces](#enlaces)  
* [Citas](#citas)  
* [Códigos](#codigos)  
* [Tablas](#tablas)  
* [Imágenes](#imagenes)  
* [Lista de chequeo](#lista-de-chequeo)  

## Conceptos
* MarkDown: Método de escritura.  

**Nota:** La sintaxis empleada, se uso para hacer esta página y puede tener comportamientos diferentes según el entorno en que se ejecute.

## Qué es Markdown
Markdown es considerado un lenguaje de marcado, ya que contiene su propia sintaxis y estrutura, tambien es considerado una herramienta de software que convierte su propia sintaxis (Markdown) en HTML.


## Encabezado
Markdown utiliza una sintaxis simple y efectiva, para los encabezados utiliza el carácter, signo o símbolo "#". Los titulos en HTML se manejan con <h1\><h2\><h3\><h4\><h5\><h6\>, Markdown utiliza esta sintaxis y maneja el "#" para establecer la relación, de la siguiente forma:  

Código:
```Markdown
# my title H1 utiliza "#"
## my title H2 utiliza "##"
### my title H3 utiliza "###"
#### my title H4 utiliza "####"
##### my title H5 utiliza "#####"
###### my title H6 utiliza "######"
```
Resultado:  

# my title H1 utiliza "#"
## my title H2 utiliza "##"
### my title H3 utiliza "###"
#### my title H4 utiliza "####"
##### my title H5 utiliza "#####"
###### my title H6 utiliza "######"



## Enfatizar
Para enfatizar un texto o una palabra se utilizan los caracteres "*" o "~" según se requiera, la palabra o texto se envuelve con estos caracteres, así:

---

<!-- italic -->
* Para letra *italica* o *cursiva* se usa un "*"   

Código:
```Markdown
Se *envuelve el texto* 
```
Resultado:  

Se *envuelve el texto*  
this is an *italic* text  

---

<!-- strong -->
* Para poner **negrita** se usa **dos** "*"   

Código:
```Markdown
Se **envuelve el texto** 
```  
Resultado:   

Se **envuelve el texto**  
this is an **strong** text

---

<!-- Bold and italic -->
* Para colocar **Negrita** y al mismo tiempo *cursiva*, se usan **tres** "*"  

Código:
```Markdown
Se ***envuelve el texto***
```  

Resultado:   

Se ***envuelve el texto***  
this is an ***Bold and italic*** text

---

<!-- strike through -->
* Para ~~subrayar~~ palabras o texto, se usan dos "~"  

Código:
```Markdown
Se ~~envuelve el texto~~ 
```  
Resultado:  

Se ~~envuelve el texto~~   
this is an ~~strikethrough~~ text

## Listas
Son enumeración de cosas, personas, cantidades, etc. Estas son muy utilies para agrupar información semejante  
fruits
<!-- UL (Listas desordenadas) -->
* **Listas desordenadas:** Estas listas se caracterizan por tener una tabulacion e iniciar con un "*", ejemplo:  

Código:
```Markdown
* Manzana  
* Naranja  
* Pera
* Banano
* etc  
```
Resultado:  

* Manzana  
* Naranja  
* Pera
* Banano
* etc  
___
<!-- OL (Listas ordenadas) -->
* **Listas ordenadas:** Estas listas se caracterizan por tener una tabulación e iniciar con numeración, ejemplo:  

Código:
```Markdown
1. Manzana
2. Naranja
3. Pera
4. Banano
5. etc
```  
Resultado:  

1. Manzana
2. Naranja
3. Pera
4. Banano
5. etc
---
* Listas con Subindices: Estas listas puden ser ordenadas o desordenadas, pero cuentan con listas dentro de un item específico, estas listas cuentan con dos espacios de tabulación y pueeden iniciar con numero o "*", ejemplo:  

Código:
```Markdown
* Manzana  
    * Verde
    * Colorada
* Naranja  
    1. Valencia
    2. Hamouti
    3. Pera
* Pera
* Banano
* etc 
```  
Resultado:  

* Manzana  
    * Verde
    * Colorada
* Naranja  
    1. Valencia
    2. Hamouti
    3. Pera
* Pera
* Banano
* etc 

## Enlaces
Los enlaces son textos que nos redigiran a un sitio o zona que nosotros configuremos
<!-- Links -->

---

* Enlace con configuración, Este enlace tiene la ventaja que nos deja elegir el texto, así:  

Código:
```Markdown
Texto elegido nos [lleva a Google](https://www.google.com) 
```  
Resultado:  

Texto elegido nos [lleva a Google](https://www.google.com) 

---
* Se puede colocar un texto extra, que aparecerá cuando se coloque el cursor sobre el enlace, así:  

Código:
```Markdown
Texto elegido nos [lleva a Google](https://www.google.com "Solo aparecerá si se coloca el cursor encima") 
```  
Resultado:  

Texto elegido nos [lleva a Google](https://www.google.com "Solo aparecerá si se coloca el cursor encima")  

---

* Enlace a una session especifica del mismo documento, Nota: 
    * El lugar para el link inicia con "#"
    * El texto debe estar en minúscula
    * Si el titulo tiene espacio se debe reemplazar por "-"
    * El titulo debe estar sin tildes así: 

Código:
```Markdown
Nos lleva a [Qué es Markdown](#que-es-markdown)
```  
Resultado:  

Nos lleva a [Qué es Markdown](#que-es-markdown)

<!-- quote (citas) -->  
## Citas
Las citas se usan para en marcar un texto

Código:
```Markdown
> Cita
>> subcita   
>> otra subcita
>
> fin
```  
Resultado:  

> Cita
>> subcita   
>> otra subcita
>
> fin

___

## Códigos
Los códigos se usan para resaltar y colocar código de cualquier tipo dentro, para usar esta sintaxis se usa las comillas invertidas ``.
<!-- code -->

---

* Código simple en un línea: Este resalta el código sin importar cual sea, ejemplo con javaScript:  

Código:
```Markdown
`console.log('hello world');` 
```  
Resultado:  

`console.log('hello world');` 

---

* Código simple en multiples líneas: Este resalta el código sin importar cual sea y recibe multiples líneas de texto, ejemplo con javaScript:  

Código:
```Markdown
    ```
    const a= 'hello world';
    console.log(a);
    ```
```
Resultado:  

```
const a= 'hello world';
console.log(a);
```

---

<!-- code with type code -->
* Código con descripción: Este resalta el código y recibe el tipo de código que contiene, tambien recibe múltiples líneas, ejemplo con javaScript:  

Código:
```Markdown
    ```javascript
    const world = "hello word";
    console.log(world);
    ```
```
Resultado:  

```javascript
const world = "hello word";
console.log(world);
```
<!-- table -->
## Tablas
Las tablas se usan para presentar información con un orden específico  
Nota:
* Los titulos de cada casilla iran en la primera fila
* La segunda fila sera conformada por guion (-)
* En la segunda fila se puede agregar el símbolo (:) según su posición el texto de la columna estará inclinado hacia un lado u otro
* Las columnas estarán finalizadas o iniciadas por el símbolo (|)  

Código:
```Markdown
|firstTitle|secondTitle|cod|
|:---------|:-----------:|---:|
|1 col     |2 col      |1|
|1 col     |2 col      |1|
|1 col     |2 col      |1|
```
Resultado:  

|firstTitle|secondTitle|cod|
|:---------|:-----------:|---:|
|1 col     |2 col      |1|
|1 col     |2 col      |1|
|1 col     |2 col      |1|

<!-- images -->
## Imágenes
Se puede adjuntar imágenes en Markdown
Recibe:
* ![Texto]: Un texto que aparecerá si la imagen no se puede cargar.
* (url local o link de internet): La url o dirección local de la ubicación de la imagen.
* (url "texto extra"): un texto que aparecerá si se pasa el cursor por encima de la imagen.

---

* Imagen desde la url en internet: Solo se busca la imagen deseada en internet  

Código:
```Markdown
![imagen logo](https://3.bp.blogspot.com/-Llh8y6sZS7o/XV58r2nymuI/AAAAAAAAWLg/2sbFXI90FFo-2i7UjJ0DQrZJpBAjn9dSQCLcBGAs/s0/vscode.png "vsCode logo por url")
```
Resultado:  

![imagen logo](https://3.bp.blogspot.com/-Llh8y6sZS7o/XV58r2nymuI/AAAAAAAAWLg/2sbFXI90FFo-2i7UjJ0DQrZJpBAjn9dSQCLcBGAs/s0/vscode.png "vsCode logo por url")
<!-- images local -->

---

* Imagen desde la url en local: Solo se busca la imagen deseada en local, para esto se recomienda crear una carpeta llamada "images" y buscar la ruta desde el directorio actual 

Código:
```Markdown
![imagen logo Local](../images/vscode.png "vsCode logo Local")
```
Resultado:  

![imagen logo Local](../images/vscode.png "vsCode logo Local")

---

* Imagen con tamaño: se puede emplear código HTML y para las imágenes nos sirve para darle un tamaño específico a la imagen, Nota: Tener cuidado con la ruta dada, cuando se pasa a producción cambia la ubicación de este archivo

Código: 

```Markdown
<img src="../../images/vscode.png" alt="imagen" width="150px"/>
```
Resultado:  

<img src="../../images/vscode.png" alt="imagen" width="150px"/>

<!-- MarkDown  -->
## Lista de chequeo
Esta lista solo se ve bien si en emplea en un repositorio como github, al mostrarse en el repositorio se vera como un listado y según su estado mostrará como chequedo o no  

Código:
```Markdown
* [x] task 1
* [ ] task 2
* [ ] task 3
* [x] task 4
```
Resultado:  

* [x] task 1
* [ ] task 2
* [ ] task 3
* [x] task 4

<!-- ancla local -->
[Volver arriba ↑](#markdowm)