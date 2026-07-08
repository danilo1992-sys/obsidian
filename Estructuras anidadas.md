# Estructuras anidadas

una estructura anidada hacer referencia a otra estructura dentro de la misma 

```go
package main

import "fmt"

func main() {
	categoria := Categoria{
		Id:     1,
		Nombre: "Hola",
		Slug:   "Hola123",
	}
	producto := Producto{
		Id:          1,
		Nombre:      "Mesa",
		Slug:        "Mesa",
		Precio:      200,
		Categoriaid: categoria,
	}
	fmt.Println(producto)
}

type Personas struct {
	Id     int
	Nombre string
	Email  string
	Edad   int
}

type Categoria struct {
	Id     int
	Nombre string
	Slug   string
}

type Producto struct {
	Id         int
	Nombre     string
	Slug       string
	Precio     int
	Categoriaid Categoria
}
```