# httpd-base

A simple Apache httpd implementation for fast website deployment.

Usage example:

```
version: "2"
services:
  httpd-server:
    image: napalmzrpi/httpd-base:latest
    container_name: httpd-server
    environment:
      - TZ=Europe/Rome
    volumes:
      - /your/dir/www/source:/var/www/site
      - /your/dir/www/log:/var/log/apache2
    ports:
      - 80:80
    restart: unless-stopped
```
