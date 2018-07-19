Symfony Demo Application — WITH BUGS!
=====================================

This is 99% an installation of the Symfony demo app, with specific bugs set on each branch.

Requirements
------------

  * PHP 7.1.3 or higher;
  * PDO-SQLite PHP extension enabled.

Installation
------------

After cloning the repository, cd into the directory and run the following commands:

```bash
$ composer install
$ mkdir var/data
$ touch var/data/blog.sqlite
$ php bin/console doctrine:database:create
$ php bin/console doctrine:schema:create
$ php bin/console doctrine:fixtures:load
```

Usage
-----

There's no need to configure anything to run the application. Just execute this
command to run the built-in web server and access the application in your
browser at <http://localhost:8000>:

```bash
$ cd symfony-demo/
$ php bin/console server:run
```

Then switch to a branch to fix a bug!
