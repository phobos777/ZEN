#1. Unbuntu 16.04,2. Docker3. acme cert and auto renew4. Domain and nodes.  

```
git clone https://github.com/phobos777/docker-zen-node && cd docker-zen-node
./install.sh stakeaddr email fqdn region
```

1. put 42 ZEN in each Transparent Address2. Setup VPS' at provider3. Setup A names at GoDaddy for each VPS4. Run script:

`./install.sh ztjcr2DSYhM44gZ3WFFeoK2hDxhmK4VP3QcgK email@example.com zennode.example.com na`

5. send 1 ZEN to Private address on node6. Check private balance:

```
docker exec zen-node gosu user zen-cli z_gettotalbalance
```

7. VPS to fully update to the latest block.status:

```
docker exec zen-node gosu user zen-cli getinfo
```
