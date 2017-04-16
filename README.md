[![](https://images.microbadger.com/badges/image/sgtsquiggs/ombi.svg)](https://microbadger.com/images/sgtsquiggs/ombi)

# ombi

This image is derived from [sgtsquiggs/alpine.mono](https://hub.docker.com/r/sgtsquiggs/alpine.mono/).

Want a Movie or TV Show on Plex or Emby? Use [Ombi](https://github.com/tidusjar/Ombi)!

## Usage
```
docker run \
    --name=ombi \
    -v <path to data>:/config \
    -e PGID=<gid> -e PUID=<uid> \
    -p 3579:3579 \
    sgtsquiggs/ombi
```

## Parameters
* `-p 3579:3579` external port 3579 mapping to internal port 3579
* `-v <path>:/config` where configuation files are stored.
* `-e PGID=<gid>` for Group ID (see below)
* `-e PUID=<uid>` for User ID (see below)

## User and Group ID
Set these to match the user/group ID of shared data volumes. Files written to these volumes will match the
provided uid/gid.

## Acknowledgements

* [linuxserver/ombi](https://github.com/linuxserver/docker-ombi)
