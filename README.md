# apache

Reemplace `$ALUMNO` por el nombre de su nombre de usuario en www.tecnologoinformatico.com

EJ: `dmascheroni`

1. Cree el directorio ~/repositorios y dentro clone el
repositorio: `https://github.com/TecnologoInformatico/AdmInf-web.git`
2. Actualice el repositorio de la lista de paquetes.
    `apt update`
3. Instalar el servidor Apache mediante apt.
4. Cree el directorio /var/www/$ALUMNO
5. Asigne como propietario del directorio su usuario.
6. Configure un nuevo Virtual host. (copiando el archivo de configuración por defecto)
  6.1. ServerName $ALUMNO.tecnologoinformatico.com
  6.2. Correo de contacto con el administrador.
  6.3. El root de la aplicación. (/var/www/$ALUMNO)
7. Modifique el archivo /etc/hosts de modo que el ServerName coincida con este equipo `127.0.0.1`.
8. Reinicie el servidor apache para que los cambios tengan efecto.
9. Copie el contenido del directorio ~/repositorios/AdmInf-web a /var/www/$ALUMNO, de tal modo que el contenido del repositorio antes clonado se encuentre en el root de la aplicación.
10. Verifique que el servidor funcione correctamente.
11. Ingrese la IP del servidor y el servername a continuación:

```json
{
    "serverName": "",
    "ip": ""
}
```
# Solucion Tarea

1- mkdir repositorios, git clone https://github.com/TecnologoInformatico/AdmInf-web.git.

2- apt update.

3- sudo apt install apache2.

4- sudo mkdir /var/www/fsalaberry.

5- sudo chown ubuntu fsalaberry.

6- cd /etc/apache2/sites-available, sudo cp 000-default.conf pp.conf, sudo nano pp.conf (se edita el servername por “fsalaberry.tecnologoinformatico.com”).

7- cd /etc, sudo nano hosts (se agrega 127.0.0.1 y fsalaberry.tecnologoinformatico.com).

8- sudo service apache2 restart.

9- cp -r AdmInf-web /var/www/fsalaberry.

10- Para probarlo entro a la ip 144.22.181.202 desde el navegador.

11- {
    "serverName": "fsalaberry.tecnologoinformatico",
    "ip": "144.22.181.202"
}
