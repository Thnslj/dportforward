# dportforward
Simplifies the process of creating port forwarding tunnels with ssh and docker

```bash
echo "test" | docker secret create ssh_password -
```

```bash
 docker service create \
    --name dportforward \
    --publish 22:22 \
    --publish 2000:2000 \
    --publish 2100:2100 \
    --publish 2200:2200 \
    --publish 2300:2300 \
    --publish 2400:2400 \
    --publish 2500:2500 \
    --constraint 'node.role == worker' \
    --secret ssh_password \
    --detach=false \
    thinus/dportforward  
```