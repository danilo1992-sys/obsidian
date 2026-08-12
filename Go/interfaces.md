---
id: interfaces
aliases:
  - interfaces
tags: []
---

# interfaces

una interfaz es un contrato de una estructura, para poder asociar la interfaz a la estructura hay que hacerlo por medio de una función  

```go
package main

import "fmt"

func main() {
	e := Estrcutura{}
	fmt.Println(e.mifuncion())
}

type ejemplo interface {
	mifuncion() string
	Calculo(n1 int, n2 int) int
}

type Estrcutura struct{}

func (*Estrcutura) mifuncion() string {
	return "texto texto"
}
```