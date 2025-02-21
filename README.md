# Docker-DuckDNS
A docker image for updating your DuckDNS records. It will execute when you start the container and then once every 24 hours after that.

Create `docker-compose.override.yml` with your TOKEN and your DOMAINS (separate each domain with colon)

```yml
services:
  duckdns:
    environment:
      TOKEN: your-duckdns-token
      DOMAINS: domain1:domain2:domain3
```

Then start it with `docker-compose up -d`

Example log:

```log
Updating DuckDNS for domain1 at 2025-02-21 17:44:26
Updating DuckDNS for domain2 at 2025-02-21 17:44:26
Updating DuckDNS for domain3 at 2025-02-21 17:44:26
```
