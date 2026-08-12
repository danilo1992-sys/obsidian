---
name: Funciones closure
description: Funciones que retornan otras funciones
---

# Funciones clousure

una función clousure retorna otra función 

```go
package main

import "fmt"

func main() {
	Tabla := tabla(5)
	for i := 1; i <= 10; i++ {
		fmt.Printf("2 x %v = %v \n", i, Tabla())
	}
}

func tabla(valor int) func() int {
	numero := valor
	sec := 0
	return func() int {
		sec++
		return numero * sec
	}
}
```

para pode ejecutar la función tendremos que utilizar una variable, a cualquier variable dentro del método main se convierte en una función de forma automática 

[Gorutines y channels ](Gorutines%20y%20channels%2037551618b69c80fcbf03e1730eec3e58.md)