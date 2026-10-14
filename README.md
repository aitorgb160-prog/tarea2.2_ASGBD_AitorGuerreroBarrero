# Instalar tres sistemas gestores de base de datos
Para esta práctica, tendremos que tener una máquina virtual con estas características:
![Caracteristicas](img/caracteristicas.png)  
![almacenamiento](img/disco.png)  
---
## 1. Desplegar Oracle Database 23ai Free con Podman
En primer lugar instalaremos Podman y descargaremos la imagen, Oracle Database se ejecuta en un contenedor administrado con Podman.  
![podman](img/podman.png)  
Creamos el contendor con la imagen de Oracle  
![contenedor](img/contenedor.png)  
Comprobamos que se ha instalado correctamente:  
![version](img/version.png)  
---
## 2. Creación del volumen y del contenedor
Creamos un volumen con nombre para conservar los datos de Oracle aunque se detenga o se recree el contenedor:
![volumen](img/creacion_vol.png)  
A continuación, creamos el contenedor y publicamos el puerto TCP 1521:
![container](img/container.png)  
Revisamos el contenedor:  
![comprobar](img/comprobacion.png)  
![healthy](img/healthy.png)  
---
## 3. Creación de usuario de trabajo en Oracle  
Accedemos a SQLplus con permisos de administrador, y comprobamos las bases de datos  
![sql](img/sql.png)  
Creamos el usuario orauser y le concedemos los permisos  
![usu](img/usu.png)  
Comprobamos la conexión:
*Incidencia con credenciales
![error](img/error.png)  
---
## 4. Desplegar PostgreSQL
Instalamos postgreSQL y sus herramientas  
![postgre](img/postgre.png)  
Iniciamos el servicio y lo habilitamos para que inicie automáticamente, también comprobamos su estado  
![conf](img/conf.png)  
Creamos la base de datos  
![creacion1](img/creacion1.png)  
![creacion2](img/creacion2.png)  
**Para crear el usuario he usado el comando: CREATE USER pguser WITH PASSWORD con mi contraseña personal**  
---
## 5. Desplegar MariaDB
Instalamos Mariadb
![maria](img/maria.png)  
Comprobamos que se ha instalado correctamente y habilitamos el servicio
![estado](img/estado.png)  
Abrimos una sesión en MariaDB y creamos la base de datos dbm
![dbm](img/dbm.png)  
Creamos el usuario con el comando **CREATE USER 'muser'@'localhost' IDENTIFIED BY 'contraseña';** y le concedemos los permisos  
![permisos](img/permisos.png)  
Probamos la conexión  
![conexion](img/conexion.png)  
-----------------------------------------------------------------------------
## 6. Comprobaciones  
![total](img/total.png) 
