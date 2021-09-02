```bash
cd docker
docker network create frontend --subnet=172.21.0.0/16
docker network create backend --subnet=172.19.0.0/16
docker-compose up --build -d
```

/etc/hosts:
```
127.0.0.1 base.docker.local basegateway.docker.local
```

project: base.docker.local:8000  
traefik: basegateway.docker.local:8088
