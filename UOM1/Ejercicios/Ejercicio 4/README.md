## Ejercicios

1. Listar todos los archivos del directorio bin.
```bash
ls /bin
```
2. Listar todos los archivos del directorio tmp.
```bash
ls /tmp
```
3. Listar todos los archivos del directorio etc que empiecen por t en orden inverso.
```bash
ls -r /etc/t*
```
4. Listar todos los archivos, incluidos ocultos, del directorio raíz.
```bash
ls -a /
```
5. Cambiarse al directorio tmp, y crear directorio PRUEBA.
```bash
cd /tmp
mkdir PRUEBA
```
6. Verificar que el directorio actual ha cambiado.
```bash
pwd
```
7. Mostrar el día y la hora actual.
```bash
date
```
8. Posicionarse en el directorio home.
```bash
cd ~
```
9. Verificar que se está en él.
```bash
pwd
```
10. Listar todos los ficheros del directorio home mostrando su número de inodo.
```bash
ls -i ~
```
11. Borrar el directorio PRUEBA.
```bash
rm -r /tmp/PRUEBA
```
12. Crear los directorios dir1, dir2 y dir3 en el directorio PRUEBA.
```bash
mkdir /tmp/PRUEBA/dir1 /tmp/PRUEBA/dir2 /tmp/PRUEBA/dir3
```
13. Dentro de dir1 crear el directorio dir11.
```bash
mkdir /tmp/PRUEBA/dir1/dir11
```
14. Dentro del directorio dir3 crear el directorio dir31.
```bash
mkdir /tmp/PRUEBA/dir3/dir31
```
15. Dentro del directorio dir31, crear los directorios dir311 y dir312.
```bash
mkdir /tmp/PRUEBA/dir3/dir31/dir311 /tmp/PRUEBA/dir3/dir31/dir312
```
16. Copiar el archivo /etc/motd a un archivo llamado mensaje de vuestro directorio PRUEBA.
```bash
cp /etc/motd /tmp/PRUEBA/mensaje
```
17. Mover el directorio dir31 y sus subdirectorios debajo de dir2.
```bash
mv /tmp/PRUEBA/dir3/dir31 /tmp/PRUEBA/dir2/
```
18. Borrar los archivos y directorios de dir1, incluido el propio directorio.
```bash
rm -r /tmp/PRUEBA/dir1
```
19. Borrar todos los archivos y directorios creados durante los ejercicios.
```bash
rm -r /tmp/PRUEBA
```