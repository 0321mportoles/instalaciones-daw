# Instalacion Drupal

## Creamos base de datos drupal, usuario y contraseña y le damos permisos.
	> mysql -u root -p
	create database drupal;
	use drupal;
	create user 'drupal'@'localhost';
	grant all privileges on drupal.* to 'drupal'@'localhost' identified by 'password';
	flush privileges;


![Captura1](capturas/config_bbdd.png)


## Descargamos drupal y lo instalamos
	> wget https://www.drupal.org/download-latest/zip
	> unzip zip

![Captura2](capturas/download_drupal.png)

Configuramos virtualhost para que el servidor responda a la url drupal.miservidor.com

![Captura3](capturas/config-vhost-drupal.png)

Habilitamos el nuevo sitio creado para poder acceder via navegador y reiniciamos Apache.

![Captura4](capturas/enable-drupal-site.png)

Actualizamos el fichero de hosts en Windows para poder acceder a nuestro servidor de forma local

![Captura5](capturas/hosts-file.png)


## Actualizamos la version de PHP porque hay incompatibilidad de versiones
![Captura17](capturas/php_upgrade/version_inicial_php.png)

Añadimos el repositorio

![Captura18](capturas/php_upgrade/anadir_repositorio.png)

Actualizamos el repositorio

![Captura19](capturas/php_upgrade/instalar_php73.png)

Deshabilitamos la version antigua de PHP y habilitamos la nueva, la 7.3

![Captura21](capturas/php_upgrade/habilitar_nueva_versionPHP.png)

![Captura20](capturas/php_upgrade/version_final_php.png)

Pantalla de bienvenida a la instalacion de Drupal

![Captura6](capturas/6_instalacion_drupal.png)

![Captura7](capturas/6_2-instalacion_drupal.png)

Para continuar nos pide instalar modulos adicionales que no estan incluidos en la instalacion por defecto de PHP, son: dom, xml, rewrite y simplexml

![Captura8](capturas/6_3-instalacion_drupal-modulos-adicionales-php.png)

![Captura9](capturas/6_4-instalacion_drupal-modulos-adicionales-php.png)

Configuramos nuestro virtualhost para aceptar URL limpias

![Captura10](capturas/6_5-instalacion_drupal-url-limpias.png)

![Captura12](capturas/6_7-instalacion_drupal-url-limpias-apache-conf.png)

![Captura11](capturas/6_6-instalacion_drupal-BBDD.png)

## Actualizamos la version de la base de datos porque hay incompatibilidad de versiones

![Captura22](capturas/update-mysql-version/1_actualizar_valores.png)

Desinstalamos la version antigua de mariadb

![Captura23](capturas/update-mysql-version/2-desintalar-mariadb-version.png)

Descargamos la nueva version y ejecutamos el instalador despues de cambiar los permisos para hacer el instalador ejecutable

![Captura24](capturas/update-mysql-version/3-instalacion-nueva-mariadb.png)

Instalamos la nueva version

![Captura25](capturas/update-mysql-version/4-instalacion-mariadb-server.png)

![Captura13](capturas/6_8-instalacion_drupal-modulos.png)

![Captura14](capturas/6_9-instalacion_drupal-info-sitio.png)

## Drupal se ha instalado correctamente
![Captura15](capturas/7-drupal-funciona-admin.png)

![Captura16](capturas/8-drupal-funciona-front.png)
