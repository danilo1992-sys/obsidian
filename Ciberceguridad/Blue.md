---
tags:
  - htb
  - windows
  - eternalblue
  - ms17-010
  - principiante
aliases:
  - Blue HTB
os: Windows
platform: HTB
---

# Blue

**Dificultad:** Principiante | **Sistema:** Windows | **Plataforma:** HTB

![[73159128-c82df480-40b3-11ea-96c2-5a4fef853991.png]]

## 1) Fase de reconocimiento

Utilizamos ping para comprobar la conexión con la maquina

```bash
ping -c 3 <IP>
```

Utilizamos nmap para ver los puertos, servicios y posibles vulnerabilidades y exportarlos a un archivo grepealble

```bash
nmap -p- --open -sS --min-rate 5000 -vvv -n -Pn <IP> -oG allports
```

![[Captura_de_pantalla_2025-08-01_112932.png]]

utilizamos la función extractPorts previamente definida en la zsh

![[Captura_de_pantalla_2025-08-01_113249.png]]

Servicios

```bash
nmap -p<Puertos> -sCV <IP> -oN targeted
```

![[Captura_de_pantalla_2025-08-01_113815.png]]

Vulnerabilidades

```bash
nmap --script vuln <ip> -v
```

![[Captura_de_pantalla_2025-08-01_114315.png]]

ya terminado el escaneo de vulnerabilidades nos nos muestra que es vulnerable a eternal blue esta vulnerabilidad se acontece en maquina con Windows 7 con el servicios de smb v1, hay muchos scripts por internet para explotar dicha vulnerabilidad pero el mas recomendado y que menos problemas da es el de metaexploit es el que voy a esta utilizando

## 2) Explotación

para utilizar metasploit tendremos que ejecutar el siguiente comando

```bash
msfconsole -q
```

el parámetro -q es para que no muestre el banner del inicio

![[Captura_de_pantalla_2025-08-01_115247.png]]

procedemos a buscar la vulnerabilidad se puede buscar tanto por el noble de la vulnerabilidad o por el cve en este caso lo busque por el nombre

```bash
search eternalblue
```

![[Captura_de_pantalla_2025-08-01_115646.png]]

hay que seleccionar el script a utilizar con el comando

```bash
use 0
```

![[Captura_de_pantalla_2025-08-01_120314.png]]

metaesploit empieza a enumerar los scripts desde el 0, después de seleccionar el script a utilizar ejecutamos el comando

```bash
show options
```

para ver las opciones de ejecución del script

![[Captura_de_pantalla_2025-08-01_120957.png]]

en este caso tendremos que configurar el RHOSTS y el LHOST, el RHOSTS es la ip de la maquina victima y el LHOST es la ip de la maquina atacante después es recomendados volver a ejecutar el comando show options para verificar que se halla configurado todo bien

```bash
set <parametro> <valor>
```

![[Captura_de_pantalla_2025-08-01_121312.png]]

después de configurar el script ejecutamos el comando

```bash
run
```

para que se ejecute.

![[Captura_de_pantalla_2025-08-01_122743.png]]

después de que termine la ejecución con el comando shell ya podremos tener acceso a la maquina victima

![[Captura_de_pantalla_2025-08-01_123218.png]]

ya estamos dentro de la maquina victima ahora no movemos el directorio Users

```bash
cd /
cd Users
```

![[Captura_de_pantalla_2025-08-01_123414.png]]

ejecutamos el comando whoami y no dice que somos nt authority\\system que es el equivalente a root en linux los que nos da acceso total.

nos dirigimos al directorio de Users y encontramos 2 usuarios

![[Captura_de_pantalla_2025-08-01_123945.png]]

ingresamos al usuario harris y dentro de Desktop encontramos la flag de users

![[Captura_de_pantalla_2025-08-01_124122.png]]

![[Captura_de_pantalla_2025-08-01_124312.png]]

y en administrator encontramos la flag de root

![[Captura_de_pantalla_2025-08-01_124837.png]]

![[Captura_de_pantalla_2025-08-01_125043.png]]
