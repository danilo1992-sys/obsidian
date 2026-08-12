---
name: Condicionales
description: Operadores de comparación y estructuras if/else/switch
---

# Condicionales

operadores de comparación

los operadores condicionales se utilizan del lado del servidor 

 

| x == y | x es igual a y |
| --- | --- |
| x ≠ y | x es distinto de y |
| x < y | x es menor que y  |
| x <= y  | x es menor o igual que y  |
| x > y | x es mayor que y  |
| x ≥ y | x es mayor o igual a y |

## if, else

la estructura if es un control de flujo que te permite saber si una condición es verdadera o falsa 

```go
func main ()  {
	edad := 17
	if edad >= 18 {
		fmt.Println("Es mayor de edad")
	} else {
		fmt.Println("Es menor de edad")
	}
}
```

## else if

en programación se considera que es un if anidado 

```go
color := "azul"
	if color == "blanco" {
		fmt.Println("La paz y la pureza")
	} else if color == "azul" {
		fmt.Println("El cielo")
	} else if color == "amarillo" {
		fmt.Println("El sol")
	} else {
		fmt.Println("No sos de uruguay")
	}
```

## Operadores lógicos

| and | && |
| --- | --- |
| or | || |
| not | !  |

### And en código

lo que hace el operador and es comprobar si se ejecuta la primera puede pasar a ejecutar la segunda opción 

```go
	color := "blanco"
	edad := 11
	if color == "azul" && edad == 18 { 
		fmt.Println("color azul y edad 18")
```

### Or en código

el operador lógico Or compara las dos variables para saber cual es la correcta, también es otra forma de hacer comprobaciones 

```go
	color := "blanco"
	edad := 11
	if color == "azul" || edad == 18 { 
		fmt.Println("color azul y edad 18")
```

### Not en código

Invierte el valor de una excepción, si es true pasa a ser false  

```go
color := "blanco"
	edad := 11
	if !(color == "azul" || edad == 18) { 
		fmt.Println("color azul y edad 18")
```

## Variables en una condición

Se declara una variable en tiempo de ejecución  

```go
if varible :=2; varible == 1{
		fmt.Println("La condicion se cumple")
	} else {
		fmt.Println("La condicion no se cumple")
	}

```

## Switch y Case

es otro tipo de comparador parecido al if 

```go
color := "blanco"
	switch color {
	case "azul":
		fmt.Println("El cielo")
		break
	case "blanco":
		fmt.Println("La paz y la pureza")
		break 
	case "amarillo":
		fmt.Println("El sol")
		break 
	default: 
		fmt.Println("No sos de uruguay")
		break 
```