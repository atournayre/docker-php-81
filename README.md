# Docker PHP

A [Docker](https://www.docker.com/)-based installer for PHP environment.

## Getting Started

1. If not already done, [install Docker Compose](https://docs.docker.com/compose/install/)
2. Run `docker-compose build --pull --no-cache` to build fresh images
3. Run `docker-compose up` (the logs will be displayed in the current shell)
4. Run `docker-compose down --remove-orphans` to stop the Docker containers.

## Features

* For development only!
* Just 1 service : PHP FPM
* Xdebug enabled
* Super-readable configuration

**Enjoy!**

## Docs

[Xdebug](docs/xdebug.md)

## Credits

Created by [Aurélien Tournayre](https://github.com/atournayre).

Based on [Symfony Docker](https://github.com/dunglas/symfony-docker).
