## Ejercicios

1. Crear los grupos sistemas y desarrollo.
```bash
sudo groupadd sistemas
sudo groupadd desarrollo
```
2. Crear los usuarios Oliver y Tom y asignarlos únicamente al grupo sistemas.
```bash
sudo useradd -m -G sistemas Oliver
sudo useradd -m -G sistemas Tom
```
3. Crear los usuarios Carla y Sara y asignarlos únicamente al grupo desarrollo.
```bash
sudo useradd -m -G desarrollo Carla
sudo useradd -m -G desarrollo Sara
```
4. El usuario Oliver crea un fichero con nombre passwords.txt en su directorio de trabajo al que únicamente él tiene acceso, tanto de lectura como de escritura.
```bash
sudo -u Oliver touch /home/Oliver/passwords.txt
sudo -u Oliver chmod 600 /home/Oliver/passwords.txt
```
5. El usuario Oliver crea un fichero ips.txt al que tengan acceso, todos los usuarios que pertenezcan al mismo grupo, tanto para leer como para escribir.
```bash
sudo -u Oliver touch /home/Oliver/ips.txt
sudo -u Oliver chmod 660 /home/Oliver/ips.txt
sudo chgrp sistemas /home/Oliver/ips.txt
```
6. La usuaria Carla crea un fichero con nombre empleados.txt al que puede acceder cualquier usuario para leer su contenido y cualquier usuario del mismo grupo para leer o escribir.
```bash
sudo -u Carla touch /home/Carla/empleados.txt
sudo -u Carla chmod 664 /home/Carla/empleados.txt
sudo chgrp desarrollo /home/Carla/empleados.txt
```
7. Crear nuevo grupo rrhh, añadiendo el usuario Pepa. Cambia el propietario y el grupo al que pertenece el fichero empleados.txt por grupo rrhh y usuario Pepa.
```bash
sudo groupadd rrhh
sudo useradd -m -G rrhh Pepa
sudo chown Pepa:rrhh /home/Carla/empleados.txt
```
8. Crear el usuario Benji perteneciente a rrhh. Dentro de su directorio de trabajo crear un archivo onboarding.txt y que tenga permisos de lectura con los demás usuarios.
```bash
sudo useradd -m -G rrhh Benji
sudo -u Benji touch /home/Benji/onboarding.txt
sudo chmod 644 /home/Benji/onboarding.txt
```
9. Crear un nuevo grupo llamado seguridad y cambiar a la usuaria Sara a este nuevo grupo. Crear un nuevo fichero vulnerabilidades.txt que solo ella pueda modificar y ver.
```bash
sudo groupadd seguridad
sudo usermod -g seguridad Sara
sudo -u Sara touch /home/Sara/vulnerabilidades.txt
sudo chmod 600 /home/Sara/vulnerabilidades.txt
```
10. La usuaria Sara crea un fichero nuevo normativa.txt que solo puedan ver y modificar ella y Tom.
```bash
sudo -u Sara touch /home/Sara/normativa.txt
sudo chown Sara:sistemas /home/Sara/normativa.txt
sudo chmod 660 /home/Sara/normativa.txt
```