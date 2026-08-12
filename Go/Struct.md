---
id: Struct
aliases:
  - Struct
tags: []
---

# Struct

una estructura es un objeto que tiene diferentes campos, es la representación contractual de distintos tipos de campos  

```go
type Personas struct {
	Id     int
	Nombre string
	Email  string
	Edad   int
}
```

la primera letra del nombre de la estructura tiene que ser en mayúsculas para que quede declarada de forma publica, los nombres de los campos al ser públicos tienen que ir en mayúscula y se le tiene que indicar el tipo de dato con el que se va a trabajar.

Para poder usar una estructura hay que crear una variable que llame a la estructura 

```go
**package main

import "fmt"

func main() {
	estructura := Personas{
		Id:     1,
		Nombre: "Danilo Caceres",
		Email:  "test@test.com",
		Edad:   33,
	}
	fmt.Println(estructura)
}

type Personas struct {
	Id     int
	Nombre string
	Email  string
	Edad   int
}**
```

existe otra forma de declarar una estructura 

```go
	p := new(estructura)
	p.Id=2
	p.Nombre="juan"
	p.Edad=22
	p.Email="hola@hola.com"

	fmt.Println(p)
```