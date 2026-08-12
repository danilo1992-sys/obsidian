---
name: "Arreglos (array) y Slices"
description: Colecciones de datos con arreglos y slices en Go
---

# Arreglos (array) y Slices

de forma fácil y sencilla. un slice  o un arreglos es una variable que permite guardar múltiples datos 

la diferencia entre slice y arreglo es que el arreglo al arreglo hay que especificarle de forma manual el lago y la cantidad de los datos que tiene que almacenar  y el slice cumple con las mismas funciones pero se le pueden agregar o modificar datos, en el array la posición inicial es 0 

### Array

```go
	 var paises [5]string
	paises[0] = "Mexico"
	paises[1] = "Argentina"
	paises[2] = "Colombia"
	paises[3] = "Peru"
	paises[4] = "Venezuela"
	fmt.Println(paises[2])
	fmt.Println("El largo del array es:", len(paises)) // el largo del array
```

en array hay que ingresar los datos de forma manual, para acceder a un dato en especifico al momento de imprimir los datos por pantallas hay que indicar la posición donde se encuentran los datos, la función  len muestra la cantidad de posiciones de un arreglo  

### Slice

```go
var paises = make([]string, 6)
	paises[0] = "Mexico"
	paises[1] = "Argentina"
	paises[2] = "Colombia"
	paises[3] = "Peru"
	paises[4] = "Venezuela"
	paises[5] = "Ecuador" 
	fmt.Println(paises[5])
	fmt.Println("El largo del array es:", len(paises)) // el largo del array

	// agregar un elemento al slice
	paises = append(paises, "Uruguay")
	fmt.Println("El nuevo largo del array es:", len(paises))
	fmt.Println(paises[6])
	
	// agregar un elemento al slice
	paises = append(paises, "Uruguay")
	fmt.Println("El nuevo largo del array es:", len(paises))
	fmt.Println(paises[6])
```

para crear un slice hay que utilizar el constructor make e indicarle de formar referencial el tamaño del arreglo  es dinámico , 

para agregar datos al slice se utiliza la función append, al intentar hacer la misma función en un arreglo normal dará un error, esto sucede por que no se puede modificar la cantidad de datos de un arreglo