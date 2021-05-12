# JSON Web Token  

## Indice
* [Conceptos](#conceptos)
* [Qué es JWT](#que-es-jwt)
* [Estructura de JWT](#estructura-de-jwt)
* [Encabezado (Header)](#encabezado-header)
* [Carga util (Payload)](#carga-util-payload)
* [Firma (Signature)](#firma-signature)
* [Más Información](#mas-informacion)

## Conceptos
* ***JWT:*** Es un estándar abierto ( RFC 7519 ) que define una forma compacta y autónoma de transmitir información.
* ***Token:*** Es una cadena de caracteres que tiene u certificado coherente en cierto lenguaje de programación.
    * **Token de seguridad** Es utilizado para facilitar el proceso de autentificación de usuarios.
    * **Tokens firmados** Estos pueden verificar la integridad de los reclamos contenidos en él.  
## Qué es JWT
Es un estándar abierto ( RFC 7519 ) que define una forma compacta y autónoma de transmitir información de forma segura entre las partes como un objeto JSON.  

## Estructura de JWT
En su forma compacta, los tokens web JSON constan de tres partes separadas por puntos (.), que son:

* header (Encabezamiento)
* payload (Carga útil)
* signature (Firma) 

Las primeras dos partes (header y payload) son strings en base64 creados a partir dos JSON. La tercer parte (signature) toma las otras dos partes y las encripta usando un algoritmo (normalmente SHA-256).  
`header.payload.signature`   

## Encabezado (Header)  

```json
{
  "alg": "HS256",
  "typ": "JWT"
}
```  
Este consta de dos partes:  
* ***(alg)*** Algoritmo de firma que se utiliza, como HMAC, SHA256 o RSA.
* ***(typ)*** Tipo de token, siempre debe ser JWT.  

## Carga util (Payload) 

Esta es la segunda parte del token y contiene la notificaciones, existen tres tipos de payload: payload registradas, públicas y privadas.  
Este es un JSON que puede tener cualquier propiedad, pero existen una serie de propiedades definidos estándar.
> Tenga en cuenta que para los tokens firmados, esta información, aunque protegida contra alteraciones, es legible por cualquier persona. *No coloque información secreta en la carga útil o en los elementos de encabezado de un JWT a menos que esté cifrada.*
* **Registered claims:** (Reclamaciones registradas) se trata de un conjunto de reclamaciones predefinidas que no son obligatorias, pero sí recomendadas, para proporcionar un conjunto de reclamaciones útiles e interoperables.  

* **Public claims:** (Reclamos públicos) estos pueden ser definidos a voluntad por aquellos que usan JWT. Pero para evitar colisiones, deben definirse en el Registro de tokens web JSON de IANA o definirse como un URI que contiene un espacio de nombres resistente a colisiones.  

* **Private claims:** (Reclamos privados) estos son reclamos personalizados creados para compartir información entre las partes que acuerdan usarlos y no sonreclamos registrados ni públicos.   

```json
{
  "sub": "1234567890",
  "name": "John Doe",
  "admin": true
}
```  
> *Tenga en cuenta que los nombres de las notificaciones tienen solo tres caracteres, ya que JWT debe ser compacto.*
* Creador (iss) - Identifica a quien creo el JWT
* Razón (sub) - Identifica la razón del JWT, se puede usar para limitar su uso a ciertos casos.
* Audiencia (aud) - Identifica quien se supone que va a recibir el JWT. Un ejemplo puede ser web, android o ios. Quien use un JWT con este campo debe además de usar el JWT enviar el valor definido en esta propiedad de alguna otra forma.
* Tiempo de expiración (exp) - Una fecha que sirva para verificar si el JWT esta vencido y obligar al usuario a volver a autenticarse.
* No antes (nbf) - Indica desde que momento se va a empezar a aceptar un JWT.
* Creado (iat) - Indica cuando fue creado el JWT.
* ID (jti) - Un identifador único para cada JWT.  

Sacado de [Platzi: Introducción a JSON Web Tokens](https://platzi.com/blog/introduccion-json-web-tokens/).  

## Firma (Signature)
   
Para crear la parte de la firma, debe tomar el encabezado codificado, la carga útil codificada, un secreto, el algoritmo especificado en el encabezado y firmarlo.  
Por ejemplo, si desea utilizar el algoritmo HMAC SHA256, la firma se creará de la siguiente manera:   
```javaScript
HMACSHA256(
  base64UrlEncode(header) + "." +
  base64UrlEncode(payload),
  secret)
```  
La firma se usa para verificar que el mensaje no se haya modificado en el camino y, en el caso de los tokens firmados con una clave privada, también puede verificar que el remitente del JWT es quien dice ser.   

El resultado son tres cadenas de URL Base64

## Más Información  

> * JSON web token ir a [JWS](https://jwt.io/ "Página oficial JWT").
> * Tokens ir a [Wikipedia](https://es.wikipedia.org/wiki/Token#:~:text=Token%20(inform%C3%A1tica)%2C%20tambi%C3%A9n%20llamado,proceso%20de%20autenticaci%C3%B3n%20de%20usuarios. "Desambiguación Token").
> * La información suminstrada es solo un resumen personal, esta es sacada y pertenece a diferentes web y sus descripciones.  

[Volver arriba](#indice)