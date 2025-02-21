# Docker-DuckDNS
A docker image for updating your DuckDNS records. It will execute when you start the container and then once every 24 hours after that.

Create `docker-compose.override.yml` with your DOMAINS and your TOKEN

```yml
services:
  duckdns:
    environment:
      TOKEN: your-duckdns-token
      DOMAINS: domain1:domain2:domain3
```

Then start it with `docker-compose up -d`
