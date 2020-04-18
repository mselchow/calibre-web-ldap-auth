# calibre-web-ldap-auth

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
