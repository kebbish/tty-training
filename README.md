# palpo-hello-docker

## Installation
You'll need
- Docker
- ...

### Build & run containers

```bash
docker build frontend -t frontend
docker build haproxy -t haproxy
docker build logstash -t logstash
```

```bash
docker run -d --name frontend -p 81:80 frontend
docker run -d --name haproxy -p 80:80 haproxy
docker run -d --name logstash -p 2000:2000 logstash
docker run -d --name mongo -p 91:27017 -p 92:28017 mongo mongod --rest --httpinterface
```

Service should be available now at <http://localhost:81> :)

## Notes & useful commands

```
docker logs <name>
```

```
docker exec -ti <name> <command>
```

```
docker inspect <name>
```
