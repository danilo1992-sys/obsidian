# Recursividad

la recursividad es cuando llamas un método se llama así mismo o cuando llamas a una función dentro del mismo método 

```go
package main

import "fmt"

func main() {
	hola(11)
}

func hola(valor int) {
	dato := valor + 1
	fmt.Println(dato)
	if dato < 10 {
		hola(dato)
	}
}
```