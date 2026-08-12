---
id: Funciones anónimas
aliases:
  - Funciones anónimas
tags: []
---

# Funciones anónimas

una función anónima no tiene nombre y se declara dentro de una variable, para utilizar la función se tiene que hacer referencia a la variable 

```go
var suma = func() {
}
```

la funciones anónima se utilizan mayormente en conexión a bases de datos 

```go
package main

import "fmt"

func main() {
	fmt.Print("La suma es ", suma(10, 12))
}

var suma = func(numero1 int, numero2 int) int {
	return numero1 + numero2
}
```