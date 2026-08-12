---
name: modulo-os
description: Interacción con el sistema operativo y creación de CLIs
---

# modulo-os

El modulo os en golang nos permite interactuar con el sistema operativo para poder maejar archivos, variables de entorno, permisos, etc

Tambien se puede usar para la creacion de cli basicas

```go
package main

import (
 "flag"
 "fmt"
)

func main() {
 nombre := flag.String("nombre", "", "El nombre es")
 edad := flag.Int("edad", 18, "La edad es")
 flag.Parse()
 fmt.Println("El nombre es", *nombre)
 fmt.Println("La edad es", *edad)
}
```
