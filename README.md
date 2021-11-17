# Hidden Service Repo
How to run a Hidden Service in I2P and Tor Network with a simple Docker-Compose file.

## Install
```bash
docker-compose build
docker-compose up -d
```

## Get .onion Hostname
```bash
docker exec -it hidden-service_tor-proxy_1 cat /var/lib/tor/hidden-service/hostname
```

## Test Tor-Proxy

```bash
curl https://check.torproject.org/api/ip
```

```bash
curl --socks5 127.0.0.1:9050 https://check.torproject.org/api/ip
```