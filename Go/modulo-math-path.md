---
id: modulo-math-path
aliases:
  - modulo-math-path
tags: []
---

# modulo-math-rath

el modulo-math-rath se utiliza para generar cadenas de texto de forma aleatoria, esto es util para generar contraseñas

## Forma 1 de uso

```go
 random := rand.Intn(101)
 fmt.Println(random)
```

## Forma 2 de uso

la forma numero 2 usa el modulo time para que sea mas rapido a la hoara de construir la contraseña

```go
 min := 10
 max := 100
 rand.Seed(time.Now().UnixNano())
 random2 := rand.Intn(max-min) + min
 fmt.Println(random2)
```
