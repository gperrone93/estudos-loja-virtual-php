# Projeto em Desenvolvimento 

Este é um projeto que faz parte do curso da HCODE 

> https://www.udemy.com/course/curso-php-7-online/ 

# Descrição do projeto 
... 


# Dependencias 

- PHP > 7.2
- phpmailer
- slim Framework
- raintpl

# Iniciando o projeto 


- Crie um banco de dados db_ecommerce e importe o arquivo DB/db_ecommerce2019.sql
- Crie uma linha no hosts do windows/ubunto com 127.0.0.1		www.gpecommerce.com.br
- Configurar o httpd-vhosts.conf do apache com as info
````
<VirtualHost *:80>
    ServerAdmin webmaster@hcode.com.br
    DocumentRoot "G:/Outros computadores/Meu computador/Novos_estudos/Udemy/php7/26-projeto-final/loja-virtual-php"
    ServerName www.gpecommerce.com.br
    ErrorLog "logs/dummy-host2.example.com-error.log"
    CustomLog "logs/dummy-host2.example.com-access.log" common
	<Directory "G:/Outros computadores/Meu computador/Novos_estudos/Udemy/php7/26-projeto-final/loja-virtual-php">
        Require all granted

        RewriteEngine On

        RewriteCond %{REQUEST_FILENAME} !-d
        RewriteCond %{REQUEST_FILENAME} !-f
        RewriteRule ^ index.php [QSA,L]
	</Directory>
</VirtualHost>

```
- Faça um composer upodate no projeto para instalar as dependencias e configurar o autoload 
