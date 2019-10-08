# traefik-compose
This repo is simple traefik in docker.

## Features
   - [x] Domain mapping
   - [x] BasicAuth
   - [x] Compress
   - [x] RateLimit

## Usage

Create `.env` file from `.env.example` 

```sh
    cp .env.example .env
```

Generate Basic authentication
`Note: all dollar signs in the hash need to be doubled for escaping.`
```sh
    echo $(htpasswd -nb user password) | sed -e s/\\$/\\$\\$/g
```

Run

```bash
    docker-compose up
```

## Endpoint
Frontend : http://localhost

Backend : http://api.localhost

Dashboard (Basic-auth) : http://dashboard.localhost

Traefik Dashboard : http://localhost:8080