---
id: logs
aliases:
  - logs
tags: []
---

# logs

en go el paquete de logs no permite estandarizar en formato de texto plano todo lo que pasa en una aplicacion de esta forma podremos resolver de forma mas eficiente los errores presentados

el argumento Fatal muestra un error y detiene el scripts en el momento

```go
log.Fatal("Error fatal en el servidor")
```

tambien existen varios tipos

```go
  log.Println("Error fatal en el servidor")
  log.Fatalf("%s Error fatal en el servidor", <Variable>)
```

log.Println no muestra un mensaje pero no detiene la ejecucion del scripts con Fatalf
podemos insertar una variable

log.panic podemos imprimir un error y que lo capture el panic por medio del reocver

```go
  log.Panicf("%s Error fatal en el servidor", <Variable>)
```

con el modulo os podemos guardar la salida de los logs en un archivo de texto

```go
f, err := os.OpenFile("logs.log", os.O_APPEND|os.O_CREATE|os.O_RDWR, 0o666)
 if err != nil {
  log.Fatal(err)
 }
 defer f.Close()
  log.SetOutput(f)
  log.Printf("Error linea %v", 1)

```
