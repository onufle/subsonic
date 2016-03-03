# subsonic

first try docker+github+dockerhub

the goal was only to validate the workflow :

Dockerfile > github > autobuild on dockerhub > docker pull

I used this source as model : https://github.com/mschuerig/docker-subsonic

Startup the container goes like this :

docker run -dit -p 4040:4040 -p 4050:4050 -v /etc/timezone:/etc/timezone:ro -v </media/directory/>:/var/music:ro -v </path/to/subsonic_data/>:/var/subsonic <Build>

Next steps are :

- understand why i get less songs with the container than with subsonic installed on the host
- deport database on a mysql container
- manage startup of the whole thing with composer
- maybe integrate a WAR push without time limitation for client app




