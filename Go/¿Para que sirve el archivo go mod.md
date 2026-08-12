---
id: "¿Para que sirve el archivo go mod"
aliases:
  - "¿Para que sirve el archivo go mod"
tags: []
---

# ¿Para que sirve el archivo go.mod?

Por convención se recomienda que el nombre del proyecto sea igual al nombre del repositorio de GitHub 

Para crear el archivo 

```bash
go mod init <nombre del projecto>
```

el archivo go.mod contiene 

```go
module clase_1 // el nombre del modulo 

go 1.22.2 // es la version de go 
```

esto sirve para que el compilador de GO entienda la aplicación como un modulo, a medida que se vallan instalado dependencias el archivo crecerá