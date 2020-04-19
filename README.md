# calibre-web-ldap-auth

EDIT: I realized after putting this together that the LinuxServer image apparently includes the necessary packages for the LDAP auth (from what I gathered from their Dockerfile). However, I've been unable to get the add-on to appear in the config. I have switched to Technosoft2000's Calibre-Web image that seems to work with LDAP auth better.

This Docker mod is meant to be used with [LinuxServer's calibre-web](https://github.com/linuxserver/docker-calibre-web) image in order to add the necessarily packages for LDAP authentication.

## Usage

In your `docker-compose.yml`, add the following under `environment`:

```
version: 3
  services:
    calibre-web:
      ...
      environment:
        - DOCKER_MODS=mselchow/calibre-web-ldap-auth:latest
```

## Configuration

See janeczku/calibre-web's wiki entry [here](https://github.com/janeczku/calibre-web/wiki/LDAP-Login).
