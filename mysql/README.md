ATCFM MySql
===========

ATCFM MySQL docker image

Build
-----

```sh
$ sudo docker build -t atcfm/mysql .
```

Setup mysql tables
------------------

```sh
$ mkdir data
$ sudo docker run -v `pwd`/data:/var/lib/mysql mysql mysql_install_db
```

Run
---

```sh
$ sudo docker run -d -v `pwd`/data:/var/lib/mysql mysql
```

Manage
------

```sh
$ sudo docker run -i -t -link mysql:mysql mysql /bin/bash -i -l
$ mysql -u root -h $MYSQL_PORT_3306_TCP_ADDR
```
