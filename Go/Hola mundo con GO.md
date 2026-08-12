---
name: Hola mundo con GO
description: Primer programa en Go y estructura básica
---

# Hola mundo con GO

el archivo principal por convenció se tiene que llamar main.go, utiliza un formato llamado hander 

```go
package <Paquete hander>
```

utilizar un paquete hander no permite modularizar por demanda, todo lo que se ejecuta en GO se hace dentro de funciones.

para declarar una función. el nombre de la función tiene que ser el nombre del paquete  

 

```go
func main(){
	fmt.Println("Hello, World!")
}
```

para importar un paquete 

```go
import "<Nombre del paquete>"
```

en este caso es el paquete fmt que sirve para mostrar una salida por pantalla 

para pode ejecutar el archivo 

```bash
go run <Nombre del archivo>
```