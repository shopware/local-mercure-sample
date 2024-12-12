# Local Mercure Example with Docker
## Introduction
This is the local mercure example with docker. It is enabled the anonymous mode, will allow all the origins, so it's only for development.

## How to run
Just run this:
```
docker-compose up
```

## Basic information

Default Hub information:
- Hub URL: `http://localhost:8081/.well-known/mercure`
- Hub subscriber secret: `MySecret`
- Hub publisher secret: `MySecret`

### Port
- Default is `8081`. 
- Change: navigate to `docker-compose.yml`, find `services => mercure => ports` and replace with new port number (e.g: `9091:80`)

### Secret Key
- Default is `MySecret`. 
- Change: navigate to `Caddyfile` and update `publisher_jwt` or `subscriber_jwt` to any value you want.
