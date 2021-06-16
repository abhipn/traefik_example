# traefik example

##### Steps
- `chmod 600 ./traefik/traefik.yml`
- `docker-compose up`

```
certificatesResolvers:
  myresolver:
    acme:
      caServer: "https://acme-staging-v02.api.letsencrypt.org/directory"
```
