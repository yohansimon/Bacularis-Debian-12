# Ligne de commande Bacularis Debian 12

Installation de Bacula et de nginx
```bash
$ apt install bacula
$ apt install nginx php-fpm
```
Installation des modules PHP
```bash
$ apt install curl patch php-cli php-bcmath php-curl php-xml php-json php-ldap php-mysql php-pdo php-pgsql php-intl
```
Téléchargement du répertoire composer
```bash
$ curl -s http://getcomposer.org/installer | php
$ mv composer.phar /usr/local/composer
$ composer create-project bacularis/bacularis-app
```

```bash
$ ls /var/run/php8.2-fpm.sock
$ protected/tools/install.sh -p /var/run/php/php8.2-fpm.sock
```
Déplacement du fichier bacularis
```bash
$ mv bacularis-nginx.conf /etc/nginx/sites-available/bacularis.conf
$ ln -s /etc/nginx/sites-available/bacularis.conf /etc/nginx/sites-enabled
```
ligne de commande à copier sur l'interface web de Bacularis
```bash
$ nano /etc/sudoers.d/bacularis
```