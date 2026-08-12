---
id: modulo-custom
aliases:
  - modulo-custom
tags: []
---

# modulo-custom

para pode crear modulos perzonalisado tendremos que crear subcarpetas dentro de la carpeta principal, el nombre del modulo declarado en el main del mismo el muy importante por que es como se le va a importar, se recomienda usar fmt solo para el debug del modulo

cumpliria la misma funcion que el archivo o la carpeta utils en alguno lenguajes

Modulo custom

```go
package moduloejemplo

func Ejemplo1() string {
 return "Hola mundo"
}

func Ejemplo2(nombre string) string {
 return "Hola " + nombre
}
```

Moin

```go
package main

import (
 "fmt"

 moduloejemplo "modulos/modulo_ejemplo"
)

func main() {
 fmt.Println(moduloejemplo.Ejemplo1())
 fmt.Println(moduloejemplo.Ejemplo2("Danilo"))
}
```
