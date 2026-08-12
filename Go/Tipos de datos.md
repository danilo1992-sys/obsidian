---
name: Tipos de datos
description: Tipos básicos y compuestos en Go (string, bool, decimal)
---

# Tipos de datos

existen 2 tipos de datos los básicos y compuestos  

los datos básicos contienen 

- bool
- string
- decimal

## String

el tipo string se puede manejar de 2 maneras, puede ser con texto de tipo corto como de tipo largo 

de tipo corto

```go
var string string = texto 
fmt.Println(string)
```

el de tipo largo se recomienda declararlo con una variable rápida

```go
textoGrande := `Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum`
fmt.Println(textoGrande)
```

## Bool

los tipos de datos booleanos se puede utilizar para determinar una condición que puede ser verdadero o falso   

```go
var estado bool = true //False
fmt.Println(estado)
```

## Decimal

el tipo de dato decimal se utiliza para guardar datos con punto de coma flotante, enteros, 

existen 2 tipos de datos faltantes de 32 y 64  

los numero enteros son aquellos que no tiene una coma, dentro de los enteros existen varios tipos, están  los int8, inst16, int32, int64, 

cada entero tiene un rango de numero 

- int8 = -128  a 127
- int16 =-  2^15 a 2^15 -1
- int32 = -2^31 a 2^31 -1
- int64 = -2^63 a 2^63 -1

existe otro tipo de entero llamado unit

- unit8 = 0 a 255
- unit16 = 0 a 2^16 -1
- unit32 = 0 a 2^32 -1
- unit64 = 0 a 2^61 -1