# subsonic

first try docker+github+dockerhub

the goal was only to validate the workflow :

Dockerfile > github > autobuild on dockerhub > docker pull

I used this [Michael Schuerig] source as model

Container startup goes like this :

```sh
docker run -dit -p 4040:4040 -p 4050:4050 -v /etc/timezone:/etc/timezone:ro -v /media/directory/:/var/music:ro -v /path/to/subsonic_data/:/var/subsonic my/subsonic_image
```

[Michael Schuerig]: <https://github.com/mschuerig/docker-subsonic>
