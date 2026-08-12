---
name: Defer y panic
description: Mecanismos de diferimiento y manejo de errores en Go
---

# Defer y panic

el panic permite mostrar un mensaje para poder detener le script con la información detallada e nivel de terminal 

```go
	defer fmt.Println("mensaje con defer")
```

lo que hace el defer es decirle al script que muestre ese mensaje cuando la aplicación se termine de ejecutar, uno de los usos es con una conexión a una base de datos, el defer se puede utilizar con funciones complejas 

el panic se utiliza para mostrar los errores de ejecución de la aplicación, al usar panic se pausa la ejecucion del programa  

```go
	a := 1
	if a == 1 {
		panic("Fallo con exito")
	}
```