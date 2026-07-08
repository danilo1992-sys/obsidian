---
id: Modulo Time
aliases:
  - Modulo Time
tags: []
---

# Modulos

para poder instalar paquetes el mejor estilo de npm hay que ir a pkg.go.dev asu ves es la documentacion oficial del paquete

esta es la forma basica de usar el modulo time

```go
package main

import (
"fmt"
"time"
)

func main() {
fmt.Print("La hora actual es: ", time.Now())
}

```

una forma de desectructurar los datos

```go

func main() {
	fmt.Print("La hora actual es: ", time.Now())

	fecha := time.Now()

	fmt.Println("The year is:", fecha.Year())
}
```
