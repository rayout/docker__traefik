# docker-compose.yml

```yml
version: '2'

services:

  proxy:
    restart: always
    image: containous/traefik:latest
    ports:
      - 80:80
      - 443:443
      - 81:81
    volumes:
      - ./traefik/traefik.toml:/traefik.toml
      - /var/run/docker.sock:/var/run/docker.sock
    network_mode: bridge
```
