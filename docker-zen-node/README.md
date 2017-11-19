# 1. Unbuntu 16.04, 2. Docker, 3. acme cert and auto renew, 4. Domain and nodes.```
git clone https://github.com/phobos777/docker-zen-node && cd docker-zen-node
./install.sh stakeaddr email fqdn region
```

-put 42 ZEN in each Transparent Address-Setup VPS' at provider-Setup A names at GoDaddy for each VPS-Run script:

`./install.sh ztjcr2DSYhM44gZ3WFFeoK2hDxhmK4VP3QcgK email@example.com zennode.example.com na`-send 1 ZEN to Private address on node-Check private balance:

```
docker exec zen-node gosu user zen-cli z_gettotalbalance
```-VPS to fully update to the latest block.status:

```
docker exec zen-node gosu user zen-cli getinfo
```
