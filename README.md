# Rapid Deployment Template for Drone CI

## Files

- [`.example.env`](.example.env) - file with environment variables to startup drone server and drone runner.
- [`docker-compose.yaml`](docker-compose.yaml) - containers startup file.
- [`example.drone.conf`](nginx/example.drone.conf) - nginx reverse proxy conf.
- [`example.drone.service`](systemd/example.drone.service) - systemd service example file.

## HOWTO

1. clone repo to ur server;
2. copy `.example.env` to `.env`;
3. set environment variables to `.env`;
4. link in filesystem `conf` files and startup this like

```shell
$ systemctl enable drone.service # or systemctl enable --now drone.service
$ systemctl start drone.service
```
