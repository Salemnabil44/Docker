Docker est un outil qui permet de créer, déployer et gérer des applications dans des conteneurs. Un conteneur est une sorte de petite boîte virtuelle qui contient tout ce dont une application a besoin pour fonctionner, comme son code, ses bibliothèques, et ses dépendances.

Taper la commande "Docker run php" , si l'image n'est pas téléchargé, Docker se chargera de télécharger la dernière image  

Pour réaliser cet exercice, voici les étapes que vous devez suivre :

### 1. Exécuter l'image Docker PHP
Tout d'abord, assurez-vous que Docker est installé sur votre machine.

Ensuite, tirez l'image Docker PHP si vous ne l'avez pas encore :

```bash
docker pull php:latest
```

### 2. Lancer un conteneur interactif avec PHP
Démarrez un conteneur Docker en mode interactif avec l'image PHP :

```bash
docker run -it php:latest php -a
```

Cette commande va démarrer un conteneur avec l'image PHP et lancer l'interpréteur PHP en mode interactif (`php -a`).

### 3. Exécuter la commande dans l'interpréteur PHP
Une fois dans l'interpréteur PHP (vous verrez une invite `php >`), exécutez la commande suivante :

```php
php > phpinfo(INFO_GENERAL);
```

Cette commande va afficher les informations générales sur la configuration PHP.

### 4. Copier le résultat
Copiez les informations affichées dans le terminal après avoir exécuté la commande. Le résultat typique devrait ressembler à ceci (les détails peuvent varier en fonction de votre environnement) :

```plaintext
php > phpinfo(INFO_GENERAL);
phpinfo()
PHP Version => 8.3.10

System => Linux fac9c6e5601f 6.6.31-linuxkit #1 SMP Thu May 23 08:36:57 UTC 2024 aarch64
Build Date => Aug  1 2024 18:50:31
Build System => Linux - Docker
Build Provider => https://github.com/docker-library/php
Configure Command =>  './configure'  '--build=aarch64-linux-gnu' '--with-config-file-path=/usr/local/etc/php' '--with-config-file-scan-dir=/usr/local/etc/php/conf.d' '--enable-option-checking=fatal' '--with-mhash' '--with-pic' '--enable-mbstring' '--enable-mysqlnd' '--with-password-argon2' '--with-sodium=shared' '--with-pdo-sqlite=/usr' '--with-sqlite3=/usr' '--with-curl' '--with-iconv' '--with-openssl' '--with-readline' '--with-zlib' '--enable-phpdbg' '--enable-phpdbg-readline' '--with-pear' '--with-libdir=lib/aarch64-linux-gnu' '--enable-embed' 'build_alias=aarch64-linux-gnu'
Server API => Command Line Interface
Virtual Directory Support => disabled
Configuration File (php.ini) Path => /usr/local/etc/php
Loaded Configuration File => (none)
Scan this dir for additional .ini files => /usr/local/etc/php/conf.d
Additional .ini files parsed => /usr/local/etc/php/conf.d/docker-php-ext-sodium.ini

PHP API => 20230831
PHP Extension => 20230831
Zend Extension => 420230831
Zend Extension Build => API420230831,NTS
PHP Extension Build => API20230831,NTS
Debug Build => no
Thread Safety => disabled
Zend Signal Handling => enabled
Zend Memory Manager => enabled
Zend Multibyte Support => provided by mbstring
Zend Max Execution Timers => disabled
IPv6 Support => enabled
DTrace Support => disabled

Registered PHP Streams => https, ftps, compress.zlib, php, file, glob, data, http, ftp, phar
Registered Stream Socket Transports => tcp, udp, unix, udg, ssl, tls, tlsv1.0, tlsv1.1, tlsv1.2, tlsv1.3
Registered Stream Filters => zlib.*, convert.iconv.*, string.rot13, string.toupper, string.tolower, convert.*, consumed, dechunk

This program makes use of the Zend Scripting Language Engine:
Zend Engine v4.3.10, Copyright (c) Zend Technologies
php > 

```

### 5. Sortir de l'interpréteur PHP et du conteneur
Après avoir copié les informations, tapez `exit` pour quitter l'interpréteur PHP :

```php
php > exit
```

Ensuite, tapez `exit` à nouveau pour quitter le conteneur Docker :

```bash
exit
```

