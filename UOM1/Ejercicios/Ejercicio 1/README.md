## Ejercicio 1. Crear una estructura de ficheros
1. Crear el directorio Task.
```bash
mkdir Task
```
2. Dentro de Task, crear dos nuevos directorios Data e Info.
```bash
mkdir Task/Data Task/Info
```
3. Crear un directorio llamado IP dentro de Data.
```bash
mkdir Task/Data/IP
```
4. Crear un fichero ip.txt con la dirección IP de la máquina desde la terminal.
```bash
hostname -I > Task/Data/IP/ip.txt
```
5. Dentro del directorio Info crear dos ficheros, uno con la información del host y uno vacío que se llame user.
```bash
hostnamectl > Task/Info/host.txt
touch Task/Info/user
```

## Ejercicio 2. Modificar una estructura de ficheros
1. Renombrar Info como Información.
```bash
mv Task/Info Task/Información
```
2. Copiar el fichero ip.txt en un nuevo directorio que se llame ip2 dentro de Task.
```bash
mkdir Task/ip2
cp Task/Data/IP/ip.txt Task/ip2/
```
3. Añadir al fichero ip.txt la cadena de texto «TheBridge».
```bash
echo "TheBridge" >> Task/Data/IP/ip.txt
```
4. Eliminar el directorio Data.
```bash
rm -r Task/Data
```
5. Sobreescribir el fichero host.txt con información de la <cabecera de Google.
```bash
curl -I https://www.google.com > Task/Información/host.txt
```