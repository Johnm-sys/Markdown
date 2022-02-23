# Introduccion a Typescript

Ducumentación [typescript](https://www.google.com)

---

## Indice  

* [Crear las primeras variables](#crear-las-primeras-variables)
* [Arreglos](#arreglos)
* [Interfaces](#interfaces)  
* [Funciones básicas](#funciones-basicas)  
* [Funciones con objetos como argumentos](#funciones-con-objetos-como-argumentos)  
* [Desestructuración de objetos](#desestructuracion-de-objetos)  
* [Desestructuración de arreglos](#desestructuracion-de-arreglos)  
* [Desestructuracion de argumentos](#desestructuracion-de-argumentos)  
* [Importaciones y exportaciones](#importaciones-y-exportaciones)  
* [Clases básicas](#clases-basicas)  
* [Constructor de una clase](#constructor-de-una-clase)
* [Extender una clase](#extender-una-clase)
* [Genéricos](#genericos)
* [Decoradores de clases](#decoradores-de-clases)
* [Encadenamiento opcional](#encadenamiento-opcional)

<br>
<br>

## Crear las primeras variables

```typescript
const nombre: string = 'john';
let hp: number = 95;
let estaVivo: boolean = true;
let diferentesTipo: string | number = 'primero 1';
diferentesTipo = 2;
```

Typescript nos ira a rrojando los diferentes errores a la hora de escribir el código, mientras que javascript nos indicara el error cuando ya este copilado el código.

<br>
<br>

## Arreglos 

```typescript
let variables: any[] = [true, 'string', 1, [], {}];
```
Es una aareglo de tipo Any, lo ideal de typescript es evitar usar este tipo.

```typescript
let variables: string = ['string', 'string2', 'string3'];
const diferenteTipo (string | number)[] = [1, 'uno', 2, 'dos', 3, 'tres'];

deferenteTipo.push(4);
deferenteTipo.push('cuatro');
```

Esto va a funcionar bien ya que le indicamos que puede ser de tipo string o number, y nos permitira agregar datos de este tipo.

<br>
<br>

## Interfaces

```typescript
// Sin definir el tipo
let personaje1 = {
    nombre: 'su nombre',
    hp: 100,
    habilidades: ['h1', 'h2', 'h3'],
};

personaje1.ciudadNatal = 'pueblo paleta';
```

Aunque sin definr el tipo nos va a funcionar la realidad es que si no inicializamos que variables se pueden utilizar tendremos problemas cuando queramos agregar un nuevo dato, para lograr definirlo podemos crear una interface, este nos ayudara a agregar propiedades que no necesitan ser inicializadas:

```typescript
interface Personaje {
    nombre: string;
    hp: number;
    habilidades: string[];
    cuidadNatal?: string;
}
```

```typescript
// Usando una interfaz para definir el tipo
let personaje1: Personaje = {
    nombre: 'su nombre',
    hp: 100,
    habilidades: ['h1', 'h2', 'h3'],
};

personaje1.ciudadNatal = 'pueblo paleta';
```
Las interfaces son elementos propios de typescript, a la hora de convertir el código a javascript que interpreta el navegador no se escribira nada de esto.

<br>
<br>

## Funciones básicas

Typescript las funciones con el tipo, nos permiten saber que retornaran y que argumentos reciben, además tambien usan el intellisense para facilitarnos la lectura y una documentación del código que vamos creando:

```javascript
function sumarJavascript(a, b) {

    return a + b

}

sumarJavascrip(1,2);
sumarJavascrip('uno', ', dos');

```

Con javascript la función no es clara de su utilidad debido a que se pueden enviar diferentes datos, se podria usar para sumar numero o concatenar, además de eso si envio algo que no se puede sumar nos mostrará el error a la hora de copilar.

```typescript
function sumartypescript(a: number, b:number): number {
    return a + b;
}

sumarJavascrip(1,2);
sumarJavascrip('uno', ', dos');

```

Con typescript podemos controlar los errores y es que en el primer uso todo saldra bien, mientras en el segundo uso nos indicara un error por que con se puede asignar un dato de tipo string a number.

```typescript
function multiplicarTypescript(numero:number, otroNumero?: number, base: number = 2): number {

    return numero * base;
}
```

En typescript es muy importante el orden de los argumentos que se pasan a la función, y es que primero van los agumentos obligatorios >> argumentos opcionales >> argumentos asugnados o por defecto.

<br>
<br>

## Funciones con objetos como argumentos

```typescript
interface Personaje = {
    nombre: string;
    pv: number;
}

function curar(personaje: Personaje, curar: number): void {
    
    personaje.pv += curar;
    console.log(personaje);
}
```

Utilizando una interface para indicar el tipo da dato (objeto) que se va a pasar y por lo mismo las propiedades de este. Se puede notar que se coloco como retorno de la funcion un 'void' que en javascript es un return 'undefined', por buenas practicas es correcto siempre colocarlo.  

<br>
<br>

## Desestructuracion de objetos

```typescript
    interface Reproductor {
        cancion: string;
        volumen: number;
        segundo: number;
        detalles: Detalles
    }

    interface Detalles {
        autor: string;
        anio: string;
    }

    const reproductor: Reproductor = {
    cancion: 'Mixes',
    volumen: 90,
    segundo: 36,
    detalles: {
        anio: 2015,
        autor: 'Edd Sherad',
    },
    };

    const autor = 'fulano';
    const { cancion, segundo, volumen, detalles } = reproductor;
    const { autor: autorDetalle } = detalles;

    console.log('El volumen actual es de: ', volumen);
    console.log('El segundo actual es de: ', segundo);
    console.log('La cancion actual es de: ', cancion);
    console.log('El Autor es de: ', autorDetalle);

```
Usando la desestructuración podremos extraer los argumentos o propiedades de un objeto, crear la interface nos ayudara mucho a saber sus propiedades antes de escribirlas (ctrl + space).

Se sugiere hacer una segunda desestructuración para extraer datos en segundo nivel o más, ademaás tambien como lo que extraemos es una propiedad de un objeto, podremos asignar a una variable nueva con el nombre que queramos.

<br>
<br>

## Desestructuracion de arreglos  

```typescript
    const dbz: string[] = [ 'Goku', 'Vegeta', 'Trunks'];

    const [ , p2, p3] = dbz;

    // console.log(' El personaje 1 es: ', p1);
    console.log(' El personaje 2 es: ', p2);
    console.log(' El personaje 3 es: ', p3);

    console.log(' El personaje 1 es: ', dbz[0]);
    console.log(' El personaje 2 es: ', dbz[1]);
    console.log(' El personaje 3 es: ', dbz[2]);

```

La desestructuración de arreglos es igual que la de objetos, con diferencia que en arreglos toma importancia la posición, además si tengo un objeto que quiero en na posicion diferente a la primera o primeras debo agregar los espacios en vez de nuevas variables.   

<br>
<br>

## Desestructuracion de argumentos

```typescript
    interface Producto {
    precio: number;
    descripcion: string;
    } 

    const nokia: Producto = {
    precio: 150,
    descripcion: 'nokia 001'
    }

    const tablet: Producto = {
    precio: 350,
    descripcion: 'tableta'
    }


    function calcularISV(productos: Producto[]): [number, number] {

    let total: number = 0;
    productos.forEach(({ precio }) => {

        total += precio;

    })

    return [total, total * 0.15];
    }

    const productos: Producto[] = [nokia, tablet];
    const [total, isv] = calcularISV(productos);

    console.log('El precio total es: ', total);
    console.log('El inpuesto total es: ', isv);   
```

La desestructuración de argumentos es util al usar metodos que nos recorren arreglos o datos, en este caso el forEach nos pide una valor para asignar el valor de cada item, con la desestruturación solo extraemos el dato que queremos y lo usamos directamente.

<br>
<br>

## Importaciones y exportaciones

```typescript
    // archivo 1
    export interface Producto {
    precio: number;
    descripcion: string;
    }

    export function calcularISV(productos: Producto[]): [number, number] {

        let total: number = 0;
        productos.forEach(({ precio }) => {

            total += precio;

        })

        return [total, total * 0.15];
    }
```
Para exportar algo y usarlo en otro archivo primero se debe exportar lo que se valla a usar en el otro archivo, se agrega la palabra **export**.
```typescript
    // archivo 2
    import { Producto, calcularISV } from './ejercicios/desestructuracion';

    const carritoDeCompra: Producto[] = [
        {
            descripcion: 'nokia',
            precio: 100
        },
        {
            descripcion: 'motorola',
            precio: 150
        }
    ]

    const [total,isv] = calcularISV(carritoDeCompra: Producto);

    console.log('El precio total es: ', total);
    console.log('El inpuesto total es: ', isv);   
```

Es necesario que todo lo que nesecitemos importar este exportado en el archivo de origien con la palara **export**, se usara la desestructuración en la importación, la inportacion se hara apuntando a el archivo origen (usar Ctrl + Space).

Nota: al importar la función se debe crear la función y esto lleva a que se ejecute lo que esta escrito en el archivo.   

<br>
<br>

## Clases basicas

```typescript
class Hero {
    private alterEgo: string;
    public edad: number;
    static nombreReal: number;
}

```
Las clases nos permiten determinar o definir si una metodo o atributo es de tipo private, public o static:
* private: Solo va ser visible dentro de esa clase.
* public: Se puede visualizar fuera de la clase.
* static: Se puede acceder al valor de la propiedad sin crear una instancia de esta.`  

```typescript
Hero.nombreReal
```

Se puede viasualizar que el nombre real de la clase se puede acceder al es sin necesidad de crear una instacia, para esto es muy util el intellisense, por el contrario los metodos y atributos de tipo private o public requiere de una instancia para poder ver que contienen.
```typescript
const ironman = new Hero();
ironman.edad    
```

las interfaces no existen en js por lo que no se visualizara en el codigo final, tabien las clases nos permiten hacer uso de metodos y dar logica a los atributos, con las interfaces no.

<br>
<br>

## Constructor de una clase

Typescript nos coloca reglas y nos ahorra trabajo e incluso nos brinda una ayuda para hacer el código mas limpio.   
constructor: El contructor es una función que se va a llamar cuando se construlla una clase, es el lugar ideal para inicializar los atributos.

```typescript
class Hero {
    alterEgo: string;
    public edad: number;
    static nombreReal: number;

    constructor (alterEgo: string) {
        this.alterEgo = alterEgo;
    }
}

const ironman = new Hero('Ironman');

```
Para inicializar los atributos se pueden enviar como parametros al crear la instancia de la clase, tambien notese que se asigna el nuevo parametro a el atributo, el parametro y el atributo se llaman igual pero se diferencian al usar el **this**.

```typescript
class Hero {
    // alterEgo: string;
    // edad: number;
    // nombreReal: number;

    constructor (
        public alterEgo: string,
        public edad?: number,
        public nombreReal?: string
        ) {}
}

const ironman = new Hero('Ironman');
const spiderman = new Hero('Spiderman', 17, 'Peter);

```

Esta forma de escritura de clases e inicializacion de los atributos nos resume el código en menos líneas, notese que se inicializan como argumentos pero tambien se les da el alcance agregando la palabra **public**

<br>
<br>

## Extender una clase

```typescript
class PersonaNormal {
    constructor(
        public nombre: string,
        public  direccion: string
    ) {}
}

class Hero extends PersonaNormal {

    constructor (
        public alterEgo: string,
        public edad?: number,
        public nombreReal?: string
        ) {
            super(nombreReal, 'New York, USA' )
        }
}
```

Si se desea convinar clases o extender la funcionalidad de las mismas se usa la palabra reservada **extends** más la clase que se va a extender.   
Para acceder y usar correctamente la clase extendida es necesario usar la funcion super dentro del contructor.   
Usamos la funcion o metodo **super** para acceder a el contructor de la clase extendida, alli colocaremos los atributos de la otra clase, uno de los atributos usados va a ser *nombreReal* este lo inicializamos en el contructor y por esto se accede a el sin la palabra **this**   

<br>
<br>

## Genericos

Se puede dar el caso de usar funciones o datos que no conocemos el tipo, para esto se le indica a la funcion que va a ser de tipo genérico, esto quiere decir que cojera el valor que se le assigne y se le indicara que tipo es, ejemplo:
```typescript
function queTipoSoy<T>(argumento: t) {
    return argumento;
}

const soyString = queTipoSoy('Soy una string');
const soyNumber = queTipoSoy(9);
```

Aunque se envien diferentes tipos de datos, el optiene el tipo y se lo asigna al argumento con ayuda de **< T >**, la T en realidad puede ser cualquier tecla pero es una standar usar esta letra.
```typescript

function queTipoSoy<T>(argumento: t) {
    return argumento;
}

const soyExplicito = queTipoSoy<number>(9);
```

Se puede enviar el tipo al que pertence explicitamente, antes de los parentecis al llamar la función se agrega el tipo que nos va a retornar.   

<br>
<br>

## Decoradores de clases

[Documentación decoradores]('https://www.typescriptlang.org/docs/handbook/decorators.html#class-decorators')


Un decorador es una funcion, esta se puede llamar y usar de diferentes maneras, aunque se suele parecer en estructura a **@miDecorador** seguido de parentecis, llaves o lo que necesite ese decorador.   
Los decoradores fucnionan a un nivel antes de crear las intancias.   
Los decoradores sirven para añadir funcionalidades a las clases.

<br>
<br>

## Encadenamiento opcional

El signo de interrogación puede significar diferentes cosas según donde se use

```typescript
interface Pasajero {
    nombre: string;
    hijos?: string[];
}

const pasajero1: Pasajero = {
    nombre: 'Fernando'
}

const pasajero2: Pasajero = {
    nombre: 'Melissa',
    hijos: ['Melissa', 'Gabriel']
}

function cuantosHijos(pasajero: Pasajero): void {

    const totalHijos = pasajero.hijos?.lenght || 0;

    console.log( totalHijos );
}

cuantosHijos( pasajero2 ); // funciona bien ya que tiene hijos
```
* Se agrega el signo **?** despues de crear una variable o atributo para indicar que puede no es obligaotrio, como en el caso de la interface el valor de *hijos?*.
* Se agrega **?** despues de leer un dato que puede ser definido o no, para evitar errores de lectura, esto devido a que si el dato no esta definido nos js intentara leer un dato *undefined* como otro dato cualquiera, al agregar este simbolo js evaluara primero si existe el dato antes de seguir usandolo.

<br>
<br>

[Volver arriba ↑](#introduccion-a-typescript)
