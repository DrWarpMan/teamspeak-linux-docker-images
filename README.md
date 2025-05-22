# About this Repo

This is a fork of the official [TeamSpeak docker repository](https://github.com/TeamSpeak-Systems/teamspeak-linux-docker-images),
all the information can be found there.

## Changes

I added the ability to set the UID and GID of the user that runs the server. Solves [#51](https://github.com/TeamSpeak-Systems/teamspeak-linux-docker-images/issues/51) and [#55](https://github.com/TeamSpeak-Systems/teamspeak-linux-docker-images/issues/55).


Example usage:
```yaml
services:
  teamspeak:
    build:
      context: https://github.com/DrWarpMan/teamspeak-linux-docker-images.git#master:alpine
    environment:
      - PUID=1000
      - PGID=1000
```