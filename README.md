# dev-https-nginx-proxy
If you just want a simple localhost https reverse proxy for your development environment. Not tested for Windows or Mac.

## Dependencies
* docker
* docker-compose

## Configuration
Change the port number in conf.d/localhost.conf
```nginx
proxy_pass http://host.docker.internal:3000;
```
from 3000 to your required port.

host.docker.internal might have some other alias for non-Linux OS.

## Run
Run with docker-compose as
```bash
docker-compose up -d
```

Read nginx stdout using
```bash
docker-compose logs
```
