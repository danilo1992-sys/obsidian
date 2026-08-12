---
id: Punteros
aliases:
  - Punteros
tags: []
---

# Punteros

un puntero te permite acceder al valor vinario de un objecto, no permite saber el valor que ocupa en la memoria.

para utilizar los puntero se tiene que usar el “&”

```go
package main

import "fmt"

func main() {
	color := "rojo"
	fmt.Print(&color)
}

```

es utilizado en los orm de base de datos