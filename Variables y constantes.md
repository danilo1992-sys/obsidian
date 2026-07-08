# Variables y constantes

## Variables

como se declaran las variables, hay 2 tipos de forma la primera es por inferencia y la segunda forma es la declaración rápida, es necesario indicar el tipo de variable 

```go
//inferecial
var nombre string 
// Para declara una variable de tipo inferencial 
nombre = "Gonzalo"

//rapida
nombre2 ;= "Hola"
```

esta es una forma de declarar variable inferenciales 

```go
var nombre string = "Gonzalo"
```

en algunos casos la variables pueden estar declaradas por fuera de la función, no es una practica recomendable  

## Constantes

Una buena practica es que las constantes se creen por fuera del método o función 

```go
const <Nombre de la constante> = <valor>
```

en la constante no es necesario declarar el tipo de dato.

poner la primera letra de la constante en mayúscula indica que puede ser utilizado por otro modulo  

lo mas utilizado en GO es la declaración corta