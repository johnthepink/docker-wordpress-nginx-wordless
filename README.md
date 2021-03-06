# docker-wordpress-nginx-wordless

This is a fork of eugeneware's [docker-wordpress-nginx](https://github.com/eugeneware/docker-wordpress-nginx), adding automatic support for [Wordless](https://github.com/welaika/wordless).

A Dockerfile that installs the latest wordpress, nginx, php-apc, php-fpm, rvm, ruby, wordless, and a bunch of gems.

NB: A big thanks to [jbfink](https://github.com/jbfink/docker-wordpress) who did most of the hard work on the wordpress parts!

You can check out his [Apache version here](https://github.com/jbfink/docker-wordpress).

## Installation

```
$ git clone https://github.com/eugeneware/docker-wordpress-nginx.git
$ cd docker-wordpress-nginx
$ sudo docker build -t="docker-wordpress-nginx" .
```

## Usage

To spawn a new instance of wordpress on port 80.  The -p 80:80 maps the internal docker port 80 to the outside port 80 of the host machien.

```bash
$ sudo docker run -p 80:80 --name docker-wordpress-nginx -d docker-wordpress-nginx
```

Start your newly created docker

```
$ sudo docker start docker-wordpress-nginx
```

After starting the docker-wordpress-nginx check to see if it started and the port mapping is correct.  This will also report the port mapping between the docker container and the host machine.
```
$ sudo docker ps

0.0.0.0:80 -> 80/tcp docker-wordpress-nginx
```

You can the visit the following URL in a browser on your host machine to get started:

```
http://127.0.0.1:80
```
