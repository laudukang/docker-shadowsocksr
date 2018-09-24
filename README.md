# Shadowsocksr in docker

## Build

update your password

```bash
cd docker-shadowsocksr
docker build -t laudukang/shadowsocksr:latest --rm .

docker run --name ssr -p 18388:18388 --restart always \
-e PASSWORD=YOUR_PASSWORD \
-e PROTOCOLPARAM=YOUR_PROTOCOLPARAM \
-e SERVER_ADDR=0.0.0.0 \
-e SERVER_PORT=18388 \
-e METHOD=none \
-e PROTOCOL=auth_chain_a \
-e OBFS=tls1.2_ticket_auth \
-e DNS_ADDR=8.8.8.8 \
-e LOG_FILE=/var/log/shadowsocks.log \
-d laudukang/shadowsocksr:latest
```

## Reference

    - [breakwa11/shadowsocksr](https://hub.docker.com/r/breakwa11/shadowsocksr/)
