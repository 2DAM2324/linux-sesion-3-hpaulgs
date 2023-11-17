# Linux Sesión 3

**Ejercicio 1**
```
Se realiza con el comando env o printenv

- SYSTEMD_EXEC_PID=1177
- SHELL=/bin/bash
- COLORTERM=truecolor
- QT_IM_MODULE=ibus
- DISPLAY=:0
````
**Ejercicio 2**
```
Lo que occure es que al utilizar el comando bash, refrescamos la terminal y es como si fuera una nueva donde no tiene la variable que anterior mente hemos creado.

- Solución:
export NOMBRE=FS

Exportaremos la variable para que aunque refresquemos la terminal, se mantenga la variable.
```
**Ejercicio 3**
```
Lo que pasa es que con las comillas dobles se usa el enter, pero con las simples no realiza el enter.
```
**Ejercicio 4**
```
Lo que ha ocurrido a sido es que ha convertido todo en carácter y no ha realizado la operación aitmética.
La forma de solucionarlo es: numero=`expr $numero + 1`
```
**Ejercicio 5**
```
nano scrip.sh
#!/bin/bash
echo Hola $1
chmod +rwx scrip.sh
./scrip.sh Paul
```
**Ejercicio 6**
```
nano scrip.sh
#!/bin/bash
echo Hola $*
./scrip.sh Paul Alex Ana Messi
```
**Ejercicio 7**
```
VAR1=hola VAR2=adios VAR3=14
a) printf "%-15s %-15s %-15d\n" $VAR1 $VAR2 $VAR3
b) Son variable locales
c) unset VAR2
d) No, debido a que son variable locales y no las hemos exportado
e) VAR0=(hola adios 14)
f) echo ${VAR0[1]}
```
**Ejercicio 8**
```
alias ne='ls -l | wc -l'
En home cambiaría el número de directorios
````
**Ejercicio 9**
```
Primer comando
find $HOME -size -1

Segundo comando 
find $HOME -size -1 > archivoP
```
**Ejercicio 10**
```
grep ejemplo *
```
**Ejercicio 11**
```
man find
man grep
```
**Ejercicio 12**
```
cat /etc/passwd | grep paulgs
```
**Ejercicio 13**
```
find $HOME ! -perm -o+r | wc -l
```
**Ejercicio 14**
```
#!/bin/bash
ls -l $1 | wc -l

chmod +x numE

./numE .
```