# Local Mercure Example with Docker
## Introduction
This is the local mercure example with docker.

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
- Anonymous mode is enabled, will allow all the origins.

### Port
- Default is `8081`. 
- Change: navigate to `docker-compose.yml`, find `services => mercure => ports` and replace with new port number (e.g: `9091:80`)

### Secret Key
- Default is `MySecret`. 
- Change: navigate to `Caddyfile` and update `publisher_jwt` or `subscriber_jwt` to any value you want.


### Production
For security reason, please follow:
- complicate the secret key.
- turn off anonymous mode.
- Specify cors_origins & publish_origins.
