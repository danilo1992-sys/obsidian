---
id: Funciones
aliases:
  - Funciones
tags: []
---

# Funciones

para declarar una función en go hay que usar la palabra reservada de func seguido de un paréntesis seguido de corchetes, el corchete de apertura tiene que ir siempre seguido de los paréntesis para evitar error de sintaxis, para poder ejecutar una función ensilla hay que llamarla desde la función principal 

función simple 

```go
package main

import "fmt"

func main() {
	hola()
}

func hola() {
	fmt.Println("Hola mundo")
}
```

función con Parámetros  

en una función con parámetros el parámetro se tiene que encontrar dentro de los paréntesis  y el tipo de datos que va a recibir 

```go
func parametros(n1 int, n2 int) {
	resultado := n1 + n2
	fmt.Println(resultado)
}
```

con retorno 

una función con retorno es un tipo de función que al terminar una tarea tiene que retornar algo, para poder utilizar el retorno tendremos que utilizar la palabra reservada de return y para mostrar en pantalla hay que utilizar println en la función principal, en el retorno es muy importante que se especifique el tipo de valor  

```go
func main() {
	hola()
}

func retorno(nombre string) string {
	return "El nombre es " + nombre
}
```

las funciones pueden retornan mas de un valor 

```go
func main() {
	nombre, edad := retornomultiple()
	fmt.Printf("Mi %v ,edad es %v \n", nombre, edad)
}

func retornomultiple() (string, int) {
	return "Danilo", 33
}
```