# gitlist Dockerfiles
## default create the container instance,just run:
```
## docker run --name mygitlist  -p 4004:80 -d ipple1986/gitlist
```
## volume the git repo,just add -v /mypath:/home/git/repositories
```
# docker run --name mygitlist -v /mypath:/home/git/repositories  -p 4004:80 -d ipple1986/gitlist
```
## use the customized config.ini,jusn add -v /mypaht/config.ini:/var/www/html/config.ini
```
# docker run --name mygitlist -v /mypath:/home/git/repositories -v /mypaht/config.ini:/var/www/html/config.ini  -p 4004:80 -d ipple1986/gitlist
```
## enter the container instance 'mygitlist',just run:
```
# docker exec -it mygitlist bash
```
