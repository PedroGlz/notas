# Configuración para hostig

* En el archivo app>Config>App.php: <br>
    colocar el dominio del host
    public string $baseURL = 'https://system-sicap.online/';

* Crear la base en el Host y colocar los datos de las credenciales en el archivo app>Config>Database.php

### Para no colocar public en la URL
    Entramos a la carpeta public y sacamos de ahí el archivo index.php y el archivo .htaccess (puede estar oculto) y colocamos los archivos en la raiz del proyecto.

### En el archivo index.php modificamos:
    
    De: require FCPATH . '../app/Config/Paths.php';
    A: require FCPATH . '/app/Config/Paths.php';

> **\* Se quitan los puntos nadamas**

* Ahora todo lo que se use de la carpeta public (img,js,css, etc..) se tiene que especificar que sale de la carpeta public

### Otro
>cuando un ajax retornn el valor concatenado con un null, imprimir con return
