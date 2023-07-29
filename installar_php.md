# Instalar PHP en windows
- Descargar la versión de Php aqui https://windows.php.net/download/
- Se descargar el ZIP la versión que diga **\"Thread Safe\"**
- Se descomprime en la raíz del disco local C
- Se modifican las **\"Variables de entorno\"**

- Al darle clic en editar, colocar en la variable **Path** la ubicación con el nombre de la carpeta php descomprimida anteriormente, por ejemplo **\"C:\\php-8.0.6;\"**
- Por ultimo, abrir el cmd y colocamos el comando **php -v** y debe salir la versión de php que se instaló, por ejempo este mensaje

```php
C:\\Users\\Pedrin>php -v
PHP 8.0.6 (cli) (built: May  4 2021 23:31:45) ( ZTS Visual C++ 2019 x64 )
Copyright (c) The PHP Group
Zend Engine v4.0.6, Copyright (c) Zend Technologies

```

## Error al instalar PHP
Si sale este error:
```php
C:\\>php -v
PHP Warning:  'C:\\Windows\\system32\\VCRUNTIME140.dll' 14.0 is not compatible with
 this PHP build linked with 14.28 in Unknown on line 0
```
Es porque debes instalar Microsoft Visual C++
debes ir a este enlace https://visualstudio.microsoft.com/es/downloads/ y ir a la parte de abajo en donde dice \"Otras plataformas y herramientas\" y descargar la opcion que se llama 
**\"Microsoft Visual C++ Redistributable para Visual Studio 2019\"**

Se descarga y se le da siguiente y siguiente y al finalizar la instalación, ejecuta el cmd y coloca **\"php -v\"** para verificar que se instaló correctamete y debe mandar la versión de PHP.