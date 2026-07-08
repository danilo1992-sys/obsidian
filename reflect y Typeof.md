# reflect y Typeof

con reflect podemos saber de forma automática el tipo de dato, para esto tendremos que utilizar la librería de reflect, 

```go
func main() {
	var string string = "Hello, World!"
	fmt.Println(reflect.TypeOf(string))
}
```

el uso es para cuando hay que hacer algún tipo de operación matemática en la aplicación 

un ejemplo es el de poder detectar el tipo de datos que devuelve una api