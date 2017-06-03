## Hexo （static website） image
# create hexo container,just run:
```
# docker run  -d --name some-hexo -p 4000:4000  ipple1986/hexo
```
# enter the hexo container ,just run:
```
# docker exec -it some-hexo bash
```
# visit the Hexo website
just visit http://127.0.0.1:4000 through your web browser. or curl http://127.0.0.1:4000
# other configuration
```
default port 4000
hexo server directory is  /opt/hexo/ipple1986 
```
