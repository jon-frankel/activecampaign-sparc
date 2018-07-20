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

  * [bug/500-error-view-post](tree/bug/500-error-view-post) -- there is an error when viewing a post
  * [bug/post-order-incorrect](tree/bug/post-order-incorrect) -- the list of posts is ordered oldest to newest, but should be newest to oldest
  * [bug/cannot-save-new-post](tree/bug/cannot-save-new-post) -- saving a new post results in an error
  * [bug/email-should-be-italicized](tree/bug/email-should-be-italicized) -- on the list of posts, the email next to the author's name should be italicized
