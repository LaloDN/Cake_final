## Cambios realizados al proyecto

1. Cambio de versión de CakePHP

Anteriormente se utilizó la versión 2.4.5 de CakePHP, ahora se actualizó por la versón 2.10.22 del framework, el cambio se encuentra principalmente en la carpeta lib del proyecto ***(Nota: la antigua carpeta de lib se encuentra en el mismo directorio pero con el nombre lib2)***

2. Transferencia de la carpeta app

El directorio app del proyecto con la versión antigua de CakePHP ha sido copiado con todos sus ficheros a la carpeta con el proyecto del servidor

3. Incorporación de plugins

El proyecto original no tenía los plugins '<a href="https://github.com/maurymmarques/minify-cakephp.git">Minify</a>' (pulsa para ir al repositorio del plugin) ni '<a href="https://github.com/FriendsOfCake/cakephp-upload">Upload</a>', por lo que se tuvieron que descargar los repositorios en las carpeta app/Plugin 

***(Nota: es importante que las carpetas sean renombradas estrictamente como "Upload" y "Minify", si no el framework tendrá problemas para reconocer los plugin y soltará un error, pero también es posible añadir estos plugins al directorio "plugins" del directorio raíz del proyecto.***

4. Correción de error de UploadBehavior

Al acceder a algunas páginas, estas soltaban un error diciendo que no se había encontrado la clase "UploadBehavior", para solucionar este error, simplemente se creó un archivo de php en la ruta app/Plugin/Upload/Model/Behavior/UploadBehavior.php con lo siguiente:

```php
<?php
class UploadBehavior extends ModelBehavior {

}
