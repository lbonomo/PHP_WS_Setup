#Personal PHP setup
`git clone git@github.com:lbonomo/PHP_WS_Setup.git PHP`

## PHP Code Sniffer

### Instalación manual
```
# Or download using wget
wget https://phars.phpcodesniffer.com/phpcs.phar -O phpcs 
wget https://phars.phpcodesniffer.com/phpcbf.phar -O phpcbf

chmod +x phpcs
chmod +x phpcbf

sudo cp phpcs /usr/bin/phpcs 
sudo cp phpcbf /usr/bin/phpcbf
```

### Rules
```
cd ~/proyectos/PHP

git clone git@github.com:WordPress/WordPress-Coding-Standards.git
git clone git@github.com:PHPCSStandards/PHPCSExtra.git
git clone git@github.com:PHPCSStandards/PHPCSUtils.git
```

### Config
Set config
```
$ sudo phpcs --config-set installed_paths "/home/lbonomo/proyectos/PHP/WordPress-Coding-Standards/,/home/lbonomo/proyectos/PHP/phpcompatibility/phpcompatibility-all/,/home/lbonomo/proyectos/PHP/phpcompatibility/phpcompatibility-wp,/home/lbonomo/proyectos/PHP/phpcompatibility/php-compatibility,/home/lbonomo/proyectos/PHP/phpcompatibility/phpcompatibility-paragonie,/home/lbonomo/proyectos/PHP/PHPCSExtra,/home/lbonomo/proyectos/PHP/PHPCSUtils/PHPCSUtils, /home/lbonomo/proyectos/PHP/PHPCSExtra/Universal, /home/lbonomo/proyectos/PHP/PHPCSExtra/NormalizedArrays"
$ sudo phpcs --config-set default_standard WordPress
```



Check config
```
$ phpcs --config-show
Using config file: /etc/php-codesniffer/CodeSniffer.conf

default_standard: WordPress
installed_paths:  /home/lbonomo/proyectos/PHP/WordPress-Coding-Standards/,/home/lbonomo/proyectos/PHP/phpcompatibility/phpcompatibility-all/,/home/lbonomo/proyectos/PHP/phpcompatibility/phpcompatibility-wp,/home/lbonomo/proyectos/PHP/phpcompatibility/php-compatibility,/home/lbonomo/proyectos/PHP/phpcompatibility/phpcompatibility-paragonie
php_path:         /usr/bin/php

$ phpcs -i
The installed coding standards are MySource, PEAR, PSR1, PSR2, PSR12, Squiz, Zend, NormalizedArrays, PHPCSUtils, Universal, WordPress, WordPress-Core, WordPress-Docs, WordPress-Extra, PHPCompatibilityWP, PHPCompatibility, PHPCompatibilityParagonieRandomCompat and PHPCompatibilityParagonieSodiumCompat
```

## Stubs

