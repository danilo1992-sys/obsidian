# instalar paquetes externos

para poder instalar un paquete externo en go hay que hacer referencia a la url absoluta del paquete sin el https

```go
  go get <url>

  go get github.com/joho/godotenv
```

despues de la instalacion se creara un archivo go.sum con las referencias de las dependencias instaldas
