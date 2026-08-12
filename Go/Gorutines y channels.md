---
id: Gorutines y channels
aliases:
  - Gorutines y channels
tags: []
---

# Gorutines y channels

los Gorutines son funciones que se pueden ejecutar en distintos canales, se puede pausar la función o enviarse a un canal, para pausar usamos el paquete time

los canales en go nos permiten dividir la ejecución de la función en varios hilos del procesador su uso es al momento de ejecutar una función muy grande o varias funciones a la vez 

ejemplo 1 

```go
package main

import (
	"fmt"
	"time"
)

func main() {
	// ejemplo 1
	fmt.Println(retorno("danilo"))
	time.Sleep(time.Second * 5)
	fmt.Println(retorno("gabriel")
}

func retorno(parametro string) string {
	return "hola  " + parametro
}
```

ejemplo 2 

```go
	canal := make(chan string)
	go func() {
		canal <- retorno("hola")
	}()
	fmt.Println(<-canal)
```