### Ambiente docker-compose Moodle 3.5 + Mysql

* Para instalação é necessário alterar a permissão da pasta **var/www**:
 ```sh
  chmod 777 -R www/
  ```

* Configurar php.ini, no repositório **/usr/local/etc/php/**
 ```sh
  cp php.ini-development php.ini
  ```
* no **php.ini** alterar o limite de upload :
```sh
upload_max_filesize 100M
post_max_size 100M
  ```
* no **etc/apache2/apache2.conf** add 
```sh
<Files ~ "^\.ht">
    Order allow,deny
    Deny from all
AcceptPathInfo On
</Files>
  ```
* Moodle 3.5: https://download.moodle.org/releases/security/


* Dentro da pasta **moodle/theme**
```sh
git clone https://github.com/CoticEaDIFRN/moodle_theme_ledor.git ledor
sudo chmod 777 -R ledor/

```
