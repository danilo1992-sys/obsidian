---
id: Modulo Time
aliases:
  - Modulo Time
tags: []
---

# Modulos

para poder instalar paquetes el mejor estilo de npm hay que ir a pkg.go.dev asu ves es la documentacion oficial del paquete

esta es la forma basica de usar el modulo time

```go
package main

import (
"fmt"
"time"
)

func main() {
fmt.Print("La hora actual es: ", time.Now())
}

```

una forma de desesctructurar los datos

```go

func main() {
 fmt.Print("La hora actual es: ", time.Now())

 fecha := time.Now()

 fmt.Println("The year is:", fecha.Year())
}
```

usando el método `<Variable>.year()` obtenemos el año y usando el método `<Variable>.Month()` obtenemos el mes en letras si lo envolvemos dentro de un int no da el numero del mes, tambien con el metodo .Day podemos saver el dia, con los metodos .Hour, .Minute y .Second se puede ver la hora los minutos y los egundos

```go
    fmt.Println("The year is: ", fecha.Year())
    fmt.Println("The month is: ", fecha.Month())
    fmt.Println("The month is: ", int(fecha.Month())
    fmt.Println("The day is:", fecha.Day())
    fmt.Println("The hour is:", fecha.Hour())
    fmt.Println("The minutes is:", fecha.Minute())
    fmt.Println("The second is:", fecha.Second())
```

para poder imprimir la fecha en formato estandar, se puede aplicar el mismo formato para las horas

```go
   fmt.Printf("%v/%v/%v \n", fecha.Day(), int(fecha.Month()), fecha.Year())
   fmt.Printf("%v:%v:%v \n", fecha.Hour(), int(fecha.Minute()), fecha.Second())
```

tambien se puede hacer operaciones con fechas ejemplo

agregar dias al fecha actual y restarle

```go
 ahora := time.Now()
 fmt.Println("Mas 22 dias: ")
 fecha1 := ahora.Add(time.Hour * 24 * 22)
 fmt.Printf("%v/%v/%v \n", fecha1.Day(), int(fecha1.Month()), fecha1.Year())
 fmt.Println("Restar")
 fmt.Println("Restar 22 dias: ")
 fecha2 := ahora.Add((time.Hour * 24 * 22) * -22)
 fmt.Printf("%v/%v/%v \n", fecha2.Day(), int(fecha2.Month()), fecha2.Year())
```

tambien se puede saver la fecha dentro de un año

```go
 fmt.Println("Dentro de 1 año: ")
 fecha3 := ahora.Add(365 * 24 * time.Hour)
 fmt.Printf("%v/%v/%v \n", fecha3.Day(), int(fecha3.Month()), fecha3.Year())
```

para que se mas facil de usar se puede usar una funcion para formatear la salida por consola

```go
func FormatoFecha(fecha time.Time) string {
 v := fmt.Sprintf("%v/%v/%v \n", fecha.Day(), int(fecha.Month()), fecha.Year())
 return v
}

```
