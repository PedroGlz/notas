# Configuración Codeignaiter para enviar correos

En el archivo:
>nombre_proyecto\app\Config\Email.php

``` php
    /**
     * The "user agent"
     */
    public string $userAgent = 'CodeIgniter';

    /**
     * The mail sending protocol: mail, sendmail, smtp
     */
    public string $protocol = 'smtp';

    /**
     * The server path to Sendmail.
     */

    public string $mailPath = '/usr/sbin/sendmail';

    /**
     * SMTP Server Address
     */
    public string $SMTPHost = 'smtp.gmail.com';

    /**
     * SMTP Username
     */
    public string $SMTPUser = 'gpedro.17.3f@gmail.com';

    /**
     * SMTP Password
     */

    // COntraseña que se genera desde el sistema de gmail en contraseña para aplicaciones y se genera esta clave
    public string $SMTPPass = 'yfavjfomutazsjyz';

    /**
     * SMTP Encryption. Either tls or ssl
     */
    public string $SMTPCrypto = 'tls';
    
    /**
     * Enable word-wrap
     */
    public bool $wordWrap = true;

    /**
     * Character count to wrap at
     */
    public int $wrapChars = 76;

    /**
     * Type of mail, either 'text' or 'html'
     */
    public string $mailType = 'html';
```

### Controlador

``` php
<?php namespace App\Controllers;

use App\Controllers\BaseController;

class Email extends BaseController
{
    public function enviar(){
        $email = \Config\Services::email();

        // $email->setFrom("correo_al_que_le_van a responder","nombre_que_envia_el_mensaje");
        // se muestra el la direccionq original que envia el correo (la que se configo en el Email)
        $email->setFrom("sicap@gmail.com","SICAP");
        // Enviar a
        $email->setTo("al221810761@gmail.com");
        // Asunto del correo
        $email->setSubject("Prueba 3");
        // Mensaje
        $email->setMessage("Cuerpo del mensaje");
        
        // Comprobacion
        if($email->send()){
            echo("ya se envio");
        }else{
            echo("no se envio");
        }
    }
}
```