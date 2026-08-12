---
name: modulo-string
description: Manipulación de cadenas de texto con strings
---

# modulo-string

el modilo strings no permite trabajar con cadenas de texto y formatearlos

## Mayucula

```go
package main

import (
 "fmt"
 "strings"
)

func main() {
 cadena := "hola mundo"
 fmt.Println(strings.ToUpper(cadena))
}
```

## Minuscula

```go
  fmt.Println(strings.ToLower(cadena))
```

con la libreria strings se puede obtener letra por letra y obtener un array con todas las letras

```go
 letras := strings.Split(cadena, "")
 fmt.Println(letras)
```

tambien se puede buscar por una palabra en especifico y saber su posicion en la cadena de texto

```go
   pos := strings.Index(cadena, "hola")
 if pos == -1 {
  fmt.Println("La palabra no esta dentro del texto", cadena)
 } else {
  fmt.Println("La palabra esta dentro del texto", cadena, "en la posicion", pos)
 }

```

tambien se puede repetir una cadena la cantidad de veces que el usuario quiera

```go
 repetidas := strings.Repeat(cadena, 10)
 fmt.Println(repetidas)
```

se puede remplazar una palabra expecifica de la cadena de texto

```go
  cadena2 := strings.Replace(cadena, "hola", "nuevo", -1)
  fmt.Println(cadena2)
```

como buscar una cadena de texto
