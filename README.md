# Docker compose of latest official Apache and PHP

This uses official docker [httpd](https://github.com/docker-library/httpd) and [php:fpm-alpine](https://github.com/docker-library/php) image.

In order to keep docker image small and perform with best performance, using `httpd:alpine` and `php:fpm-alpine`, with limited set of modules.

Run image by starting [Docker](https://www.docker.com/products/docker-desktop) and execute `docker-compose up --force-recreate`

## Experiencing sharing files issue on Windows

If running on Windows and experiencing firewall issue sharing files, fallow details in

* <https://success.docker.com/article/error-a-firewall-is-blocking-file-sharing-between-windows-and-the-containers>
* <https://stackoverflow.com/questions/42203488/settings-to-windows-firewall-to-allow-docker-for-windows-to-share-drive>

## How to test Github Actions

1. Install <https://github.com/nektos/act>
2. Run Docker and execute `act` (Notice: in first time it will run very very long, because it will download 18.2GB nektos/act-environments-ubuntu image defined in .actrc configuration)
