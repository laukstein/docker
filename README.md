# Docker compose of latest official Apache and PHP

This uses official docker [httpd](https://github.com/docker-library/httpd) and [php:fpm-alpine](https://github.com/docker-library/php) image.

In order to keep docker image small and perform with best performance, using `httpd:alpine` and `php:fpm-alpine`, with limited set of modules.

Run image by starting [Docker](https://www.docker.com/products/docker-desktop) and running `docker-compose up --build`

If running on Windows and experiencing firewall issue sharing files, fallow details in <https://success.docker.com/article/error-a-firewall-is-blocking-file-sharing-between-windows-and-the-containers> and <https://stackoverflow.com/questions/42203488/settings-to-windows-firewall-to-allow-docker-for-windows-to-share-drive>
