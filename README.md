# [**SC-N**](https://github.com/sc-n) docker-compose
### Based on [*Docker4Drupal*](https://github.com/wodby/docker4drupal)

### Notes:
* web/{drupal-folders-and-files}
* "web" is site folder. There should be index.php
* Bash aliases for Docker compose:
    * alias d-drush="docker-compose exec --user 82 php drush"
    * alias d-composer="docker-compose exec --user 82 php composer"
* edit PROJECT_NAME variable in .env file

# 
# 
# 

# Docker-based Drupal stack

[![Documentation Status](https://readthedocs.org/projects/docker4drupal/badge/?version=latest)](http://docs.docker4drupal.org)
[![Build Status](https://travis-ci.org/wodby/docker4drupal.svg?branch=master)](https://travis-ci.org/wodby/docker4drupal)
[![Wodby Slack](http://slack.wodby.com/badge.svg)](http://slack.wodby.com)
[![Wodby Twitter](https://img.shields.io/twitter/follow/wodbyhq.svg?style=social&label=Follow)](https://twitter.com/wodbyhq)

## Introduction

Docker4Drupal is a set of docker images optimized for Drupal. Use docker-compose.yml file from this repository to spin up local environment on Linux, Mac OS X and Windows. 

Read [**Getting Started**](http://docs.docker4drupal.org/en/latest/).

## Stack

[wodby/drupal-nginx]: https://github.com/wodby/drupal-nginx
[wodby/drupal]: https://github.com/wodby/drupal
[wodby/drupal-php]: https://github.com/wodby/drupal-php
[wodby/mariadb]: https://github.com/wodby/mariadb
[wodby/redis]: https://github.com/wodby/redis
[wodby/drupal-varnish]: https://github.com/wodby/drupal-varnish
[wodby/drupal-solr]: https://github.com/wodby/drupal-solr
[wodby/memcached]: https://github.com/wodby/memcached
[phpmyadmin/phpmyadmin]: https://hub.docker.com/r/phpmyadmin/phpmyadmin
[mailhog/mailhog]: https://hub.docker.com/r/mailhog/mailhog
[_/node]: https://hub.docker.com/_/node
[_/traefik]: https://hub.docker.com/_/traefik

The Drupal stack consist of the following containers:

| Container | Versions | Service name | Image | Enabled by default |
| --------- | -------- | ------------ | ----- | ------------------ |
| Nginx      | 1.10               | nginx     | [wodby/drupal-nginx]    | ✓ |
| Drupal     | 8, 7, 6            | php       | [wodby/drupal]          | ✓ |
| PHP        | 5.3, 5.6, 7.0, 7.1 | php       | [wodby/drupal-php]      |   |
| MariaDB    | 10.1               | mariadb   | [wodby/mariadb]         | ✓ |
| Redis      | 3.2                | redis     | [wodby/redis]           |   |
| Varnish    | 4.1                | varnish   | [wodby/drupal-varnish]  |   |
| Solr       | 5.5, 6.3, 6.4      | solr      | [wodby/drupal-solr]     |   |
| Memcached  | 1.4                | memcached | [wodby/memcached]       |   |
| Mailhog    | latest             | mailhog   | [mailhog/mailhog]       | ✓ |
| phpMyAdmin | latest             | pma       | [phpmyadmin/phpmyadmin] |   |
| Node.js    | 7                  | node      | [_/node]                |   |
| Traefik    | latest             | traefik   | [_/traefik]             | ✓ |

Supported Drupal versions: 6, 7, 8.

## Documentation

Full documentation is available at http://docs.docker4drupal.org/.

## Deployment

Deploy docker-based Drupal stack to your own server via [![Wodby](https://www.google.com/s2/favicons?domain=wodby.com) Wodby](https://cloud.wodby.com/stackhub/ada51e9b-2204-45ee-8e49-a4151912a168/detail).

## License

This project is licensed under the MIT open source license.
